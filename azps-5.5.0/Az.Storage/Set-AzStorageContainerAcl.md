---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190705"
---
# <span data-ttu-id="ca6d6-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ca6d6-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="ca6d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6d6-103">저장소 컨테이너에 대한 공용 액세스 권한을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="ca6d6-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca6d6-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ca6d6-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca6d6-105">DESCRIPTION</span></span>
<span data-ttu-id="ca6d6-106">**Set-AzStorageContainerAcl** cmdlet은 Azure에서 지정된 저장소 컨테이너에 대한 공용 액세스 권한을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="ca6d6-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca6d6-107">EXAMPLES</span></span>

### <span data-ttu-id="ca6d6-108">예제 1: 이름으로 Azure Storage 컨테이너 ACL 설정</span><span class="sxs-lookup"><span data-stu-id="ca6d6-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="ca6d6-109">이 명령은 공용 액세스 권한이 없는 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="ca6d6-110">예제 2: 파이프라인을 사용하여 Azure Storage 컨테이너 ACL 설정</span><span class="sxs-lookup"><span data-stu-id="ca6d6-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="ca6d6-111">이 명령은 이름이 컨테이너로 시작하는 모든 저장소 컨테이너를 얻은 다음 파이프라인의 결과를 전달하여 Blob 액세스에 대한 권한을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="ca6d6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca6d6-112">PARAMETERS</span></span>

### <span data-ttu-id="ca6d6-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca6d6-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ca6d6-114">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ca6d6-115">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ca6d6-116">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ca6d6-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ca6d6-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ca6d6-118">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ca6d6-119">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ca6d6-120">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ca6d6-121">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ca6d6-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ca6d6-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ca6d6-123">-Context</span></span>
<span data-ttu-id="ca6d6-124">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ca6d6-125">New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ca6d6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6d6-126">-DefaultProfile</span></span>
<span data-ttu-id="ca6d6-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca6d6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ca6d6-128">-Name</span></span>
<span data-ttu-id="ca6d6-129">컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="ca6d6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca6d6-130">-PassThru</span></span>
<span data-ttu-id="ca6d6-131">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca6d6-132">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca6d6-133">-Permission</span><span class="sxs-lookup"><span data-stu-id="ca6d6-133">-Permission</span></span>
<span data-ttu-id="ca6d6-134">이 컨테이너에 대한 공용 액세스 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="ca6d6-135">기본적으로 컨테이너 및 컨테이너 안의 모든 Blob은 저장소 계정의 소유자만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="ca6d6-136">익명 사용자에게 컨테이너 및 해당 Blob에 대한 읽기 권한을 부여하려면 공용 액세스를 사용하도록 컨테이너 권한을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="ca6d6-137">익명 사용자는 요청을 인증하지 않고 공개적으로 사용 가능한 컨테이너에서 Blob을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="ca6d6-138">이 매개 변수에 허용되는 값은 --Container입니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="ca6d6-139">컨테이너 및 해당 Blob에 대한 전체 읽기 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="ca6d6-140">클라이언트는 익명 요청을 통해 컨테이너의 Blob을 열회할 수 있지만 저장소 계정에서 컨테이너를 열회할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="ca6d6-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-141">--Blob.</span></span>
<span data-ttu-id="ca6d6-142">익명 요청을 통해 컨테이너의 Blob 데이터에 대한 읽기 액세스를 제공하지만 컨테이너 데이터에 대한 액세스는 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="ca6d6-143">클라이언트는 익명 요청을 사용하여 컨테이너에 Blob을 열회할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="ca6d6-144">--Off.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-144">--Off.</span></span>
<span data-ttu-id="ca6d6-145">저장소 계정 소유자만 액세스를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-145">Restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="ca6d6-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca6d6-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ca6d6-147">요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ca6d6-148">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="ca6d6-149">각 요청에 대한 서버 쪽 시간제한입니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="ca6d6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6d6-150">CommonParameters</span></span>
<span data-ttu-id="ca6d6-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6d6-152">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca6d6-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6d6-153">입력</span><span class="sxs-lookup"><span data-stu-id="ca6d6-153">INPUTS</span></span>

### <span data-ttu-id="ca6d6-154">System.String</span><span class="sxs-lookup"><span data-stu-id="ca6d6-154">System.String</span></span>

### <span data-ttu-id="ca6d6-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca6d6-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca6d6-156">출력</span><span class="sxs-lookup"><span data-stu-id="ca6d6-156">OUTPUTS</span></span>

### <span data-ttu-id="ca6d6-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ca6d6-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="ca6d6-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca6d6-158">NOTES</span></span>

## <span data-ttu-id="ca6d6-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca6d6-159">RELATED LINKS</span></span>

[<span data-ttu-id="ca6d6-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ca6d6-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="ca6d6-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ca6d6-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="ca6d6-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ca6d6-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


