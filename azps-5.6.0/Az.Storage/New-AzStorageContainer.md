---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: d726ec3fe70ca329f6e5c07ea7aae46de4ad048a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002544"
---
# <span data-ttu-id="055dd-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="055dd-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="055dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="055dd-102">SYNOPSIS</span></span>
<span data-ttu-id="055dd-103">Azure Storage 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="055dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="055dd-104">SYNTAX</span></span>

### <span data-ttu-id="055dd-105">ContainerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="055dd-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="055dd-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="055dd-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="055dd-107">설명</span><span class="sxs-lookup"><span data-stu-id="055dd-107">DESCRIPTION</span></span>
<span data-ttu-id="055dd-108">**New-AzStorageContainer** cmdlet은 Azure 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="055dd-109">예제</span><span class="sxs-lookup"><span data-stu-id="055dd-109">EXAMPLES</span></span>

### <span data-ttu-id="055dd-110">예제 1: Azure Storage 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="055dd-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="055dd-111">이 명령은 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-111">This command creates a storage container.</span></span>

### <span data-ttu-id="055dd-112">예제 2: 여러 Azure Storage 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="055dd-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="055dd-113">이 예제에서는 여러 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="055dd-114">.NET **String** 클래스의 분할  메서드를 사용하여 파이프라인의 이름을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="055dd-115">예제 3: 암호화 범위를 사용하여 Azure Storage 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="055dd-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="055dd-116">이 명령은 기본 암호화 범위를 myencryptscope로 사용하여 저장소 컨테이너를 만들고, 다른 암호화 범위를 사용하여 Blob 업로드를 이 컨테이너에 미리 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="055dd-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="055dd-117">PARAMETERS</span></span>

### <span data-ttu-id="055dd-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="055dd-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="055dd-119">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="055dd-120">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="055dd-121">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="055dd-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="055dd-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="055dd-123">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="055dd-124">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="055dd-125">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="055dd-126">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="055dd-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-127">The default value is 10.</span></span>

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

### <span data-ttu-id="055dd-128">-Context</span><span class="sxs-lookup"><span data-stu-id="055dd-128">-Context</span></span>
<span data-ttu-id="055dd-129">새 컨테이너에 대한 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="055dd-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="055dd-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="055dd-131">모든 쓰기에 대해 지정된 암호화 범위를 사용하기 위해 컨테이너를 기본값으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055dd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055dd-132">-DefaultProfile</span></span>
<span data-ttu-id="055dd-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="055dd-134">-Name</span><span class="sxs-lookup"><span data-stu-id="055dd-134">-Name</span></span>
<span data-ttu-id="055dd-135">새 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="055dd-136">-권한</span><span class="sxs-lookup"><span data-stu-id="055dd-136">-Permission</span></span>
<span data-ttu-id="055dd-137">이 컨테이너에 대한 공용 액세스 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="055dd-138">기본적으로 컨테이너 및 해당 컨테이너의 모든 Blob은 저장소 계정 소유자만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="055dd-139">익명 사용자에게 컨테이너 및 해당 Blob에 대한 읽기 권한을 부여하려면 공용 액세스를 사용하도록 컨테이너 권한을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="055dd-140">익명 사용자는 요청을 인증하지 않고 공개적으로 사용 가능한 컨테이너에서 Blob을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="055dd-141">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="055dd-142">컨테이너.</span><span class="sxs-lookup"><span data-stu-id="055dd-142">Container.</span></span>
<span data-ttu-id="055dd-143">컨테이너 및 해당 Blob에 대한 전체 읽기 액세스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="055dd-144">클라이언트는 익명 요청을 통해 컨테이너에 Blob을 열소할 수 있지만 저장소 계정에서 컨테이너를 열 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="055dd-145">Blob입니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-145">Blob.</span></span>
<span data-ttu-id="055dd-146">익명 요청을 통해 컨테이너 전체에서 Blob 데이터에 대한 읽기 액세스를 제공하지만 컨테이너 데이터에 대한 액세스는 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="055dd-147">클라이언트는 익명 요청을 사용하여 컨테이너에 Blob을 열소할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="055dd-148">끄기.</span><span class="sxs-lookup"><span data-stu-id="055dd-148">Off.</span></span>
<span data-ttu-id="055dd-149">저장소 계정 소유자만 액세스를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-149">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055dd-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="055dd-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="055dd-151">컨테이너 기본값에서 암호화 범위의 오버라이드를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055dd-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="055dd-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="055dd-153">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="055dd-154">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="055dd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055dd-155">CommonParameters</span></span>
<span data-ttu-id="055dd-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="055dd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055dd-157">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="055dd-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055dd-158">입력</span><span class="sxs-lookup"><span data-stu-id="055dd-158">INPUTS</span></span>

### <span data-ttu-id="055dd-159">System.String</span><span class="sxs-lookup"><span data-stu-id="055dd-159">System.String</span></span>

### <span data-ttu-id="055dd-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="055dd-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="055dd-161">출력</span><span class="sxs-lookup"><span data-stu-id="055dd-161">OUTPUTS</span></span>

### <span data-ttu-id="055dd-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="055dd-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="055dd-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="055dd-163">NOTES</span></span>

## <span data-ttu-id="055dd-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="055dd-164">RELATED LINKS</span></span>

[<span data-ttu-id="055dd-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="055dd-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="055dd-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="055dd-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="055dd-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="055dd-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


