export dockerBaseRun=" -e LOCAL_USER_ID=`id -u $USER` "
export LOCAL_USER_ID=`id -u $USER`

docker build -f Dockerfile.chain.testing -t chain.testing .

cd Scripts/tests


echo "--- Test 3 - serve hc.cluster.sync"
./test.hc.cluster.sync.test  hc.cluster.sync passed failed 5 "hc.cluster.sync 5 instances" && echo "--- passed" || echo "--- failed"
echo