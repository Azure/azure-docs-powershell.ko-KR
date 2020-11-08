---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041848"
---
# <span data-ttu-id="83114-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="83114-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="83114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83114-102">SYNOPSIS</span></span>
<span data-ttu-id="83114-103">저장소 컨테이너에 대 한 공용 액세스 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="83114-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83114-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="83114-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83114-105">DESCRIPTION</span></span>
<span data-ttu-id="83114-106">**Set-AzStorageContainerAcl** Cmdlet은 Azure의 지정 된 저장소 컨테이너에 대 한 공용 액세스 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="83114-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83114-107">EXAMPLES</span></span>

### <span data-ttu-id="83114-108">예제 1: 이름별로 azure storage 컨테이너 ACL 설정</span><span class="sxs-lookup"><span data-stu-id="83114-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="83114-109">이 명령은 공용 액세스 권한이 없는 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83114-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="83114-110">예제 2: 파이프라인을 사용 하 여 azure storage 컨테이너 ACL 설정</span><span class="sxs-lookup"><span data-stu-id="83114-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="83114-111">이 명령은 이름이 컨테이너로 시작 하는 모든 저장소 컨테이너를 가져온 다음 파이프라인에 해당 결과를 전달 하 여 해당 파일에 대 한 권한을 모두 Blob 액세스로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="83114-112">변수</span><span class="sxs-lookup"><span data-stu-id="83114-112">PARAMETERS</span></span>

### <span data-ttu-id="83114-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83114-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="83114-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="83114-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="83114-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83114-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="83114-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="83114-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="83114-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="83114-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="83114-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="83114-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="83114-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="83114-122">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83114-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="83114-123">-Context</span></span>
<span data-ttu-id="83114-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="83114-125">New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83114-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83114-126">-DefaultProfile</span></span>
<span data-ttu-id="83114-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83114-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83114-128">-이름</span><span class="sxs-lookup"><span data-stu-id="83114-128">-Name</span></span>
<span data-ttu-id="83114-129">컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-129">Specifies a container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83114-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83114-130">-PassThru</span></span>
<span data-ttu-id="83114-131">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83114-132">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-132">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83114-133">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="83114-133">-Permission</span></span>
<span data-ttu-id="83114-134">이 컨테이너에 대 한 공용 액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="83114-135">기본적으로 컨테이너 및 그 안의 모든 blob에는 저장소 계정의 소유자만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="83114-136">컨테이너 및 해당 blob에 대 한 읽기 권한을 익명 사용자에 게 부여 하려면 공용 액세스를 사용 하도록 컨테이너 사용 권한을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="83114-137">익명 사용자는 요청을 인증 하지 않고 공개적으로 사용할 수 있는 컨테이너에서 blob을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="83114-138">이 매개 변수에 허용 되는 값은--컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="83114-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="83114-139">컨테이너 및 해당 blob에 대 한 전체 읽기 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="83114-140">클라이언트는 익명 요청을 통해 컨테이너의 blob을 열거할 수 있지만 저장소 계정의 컨테이너를 열거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="83114-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="83114-141">--Blob.</span></span>
<span data-ttu-id="83114-142">익명 요청을 통해 컨테이너의 blob 데이터에 대 한 읽기 액세스를 제공 하지만 컨테이너 데이터에 대 한 액세스는 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="83114-143">클라이언트는 익명 요청을 사용 하 여 컨테이너의 blob을 열거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="83114-144">--Off.</span><span class="sxs-lookup"><span data-stu-id="83114-144">--Off.</span></span>
<span data-ttu-id="83114-145">저장소 계정 소유자만 액세스를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83114-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83114-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="83114-147">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="83114-148">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="83114-149">각 요청에 대 한 서버 쪽 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="83114-149">Server side time out for each request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83114-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83114-150">CommonParameters</span></span>
<span data-ttu-id="83114-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83114-152">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83114-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83114-153">입력</span><span class="sxs-lookup"><span data-stu-id="83114-153">INPUTS</span></span>

### <span data-ttu-id="83114-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="83114-154">System.String</span></span>

### <span data-ttu-id="83114-155">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="83114-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="83114-156">출력</span><span class="sxs-lookup"><span data-stu-id="83114-156">OUTPUTS</span></span>

### <span data-ttu-id="83114-157">WindowsAzure. ResourceModel를 AzureStorageContainer로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="83114-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="83114-158">상속자</span><span class="sxs-lookup"><span data-stu-id="83114-158">NOTES</span></span>

## <span data-ttu-id="83114-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83114-159">RELATED LINKS</span></span>

[<span data-ttu-id="83114-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="83114-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="83114-161">새로운 AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="83114-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="83114-162">제거-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="83114-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


