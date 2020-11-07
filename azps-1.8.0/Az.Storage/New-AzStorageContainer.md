---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: c95fcb42f403025399185f224a1438eac0f72867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698620"
---
# <span data-ttu-id="6ba04-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6ba04-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="6ba04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ba04-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba04-103">Azure 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="6ba04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ba04-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6ba04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6ba04-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba04-106">**AzStorageContainer** Cmdlet은 Azure 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="6ba04-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6ba04-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba04-108">예제 1: Azure storage 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="6ba04-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="6ba04-109">이 명령은 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-109">This command creates a storage container.</span></span>

### <span data-ttu-id="6ba04-110">예제 2: 여러 Azure storage 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="6ba04-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="6ba04-111">이 예제에서는 저장소 컨테이너를 여러 개 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="6ba04-112">.NET **문자열** 클래스의 **Split** 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="6ba04-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ba04-113">PARAMETERS</span></span>

### <span data-ttu-id="6ba04-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ba04-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6ba04-115">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6ba04-116">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6ba04-117">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6ba04-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ba04-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ba04-119">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6ba04-120">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6ba04-121">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6ba04-122">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6ba04-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-123">The default value is 10.</span></span>

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

### <span data-ttu-id="6ba04-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="6ba04-124">-Context</span></span>
<span data-ttu-id="6ba04-125">새 컨테이너에 대 한 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="6ba04-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba04-126">-DefaultProfile</span></span>
<span data-ttu-id="6ba04-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba04-128">-이름</span><span class="sxs-lookup"><span data-stu-id="6ba04-128">-Name</span></span>
<span data-ttu-id="6ba04-129">새 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-129">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="6ba04-130">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="6ba04-130">-Permission</span></span>
<span data-ttu-id="6ba04-131">이 컨테이너에 대 한 공용 액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="6ba04-132">기본적으로 컨테이너 및 그 안의 모든 blob에는 저장소 계정의 소유자만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="6ba04-133">컨테이너 및 해당 blob에 대 한 읽기 권한을 익명 사용자에 게 부여 하려면 공용 액세스를 사용 하도록 컨테이너 사용 권한을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="6ba04-134">익명 사용자는 요청을 인증 하지 않고 공개적으로 사용할 수 있는 컨테이너에서 blob을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="6ba04-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ba04-136">컨트롤러.</span><span class="sxs-lookup"><span data-stu-id="6ba04-136">Container.</span></span>
<span data-ttu-id="6ba04-137">컨테이너 및 해당 blob에 대 한 전체 읽기 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="6ba04-138">클라이언트는 익명 요청을 통해 컨테이너의 blob을 열거할 수 있지만 저장소 계정의 컨테이너를 열거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="6ba04-139">블.</span><span class="sxs-lookup"><span data-stu-id="6ba04-139">Blob.</span></span>
<span data-ttu-id="6ba04-140">익명 요청을 통해 컨테이너 전체의 blob 데이터에 대 한 읽기 액세스를 제공 하지만 컨테이너 데이터에 대 한 액세스는 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="6ba04-141">클라이언트는 익명 요청을 사용 하 여 컨테이너의 blob을 열거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="6ba04-142">끄십시오.</span><span class="sxs-lookup"><span data-stu-id="6ba04-142">Off.</span></span>
<span data-ttu-id="6ba04-143">이는 저장소 계정 소유자 에게만 액세스를 제한 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba04-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ba04-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6ba04-145">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6ba04-146">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6ba04-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba04-147">CommonParameters</span></span>
<span data-ttu-id="6ba04-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba04-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ba04-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba04-150">입력</span><span class="sxs-lookup"><span data-stu-id="6ba04-150">INPUTS</span></span>

### <span data-ttu-id="6ba04-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ba04-151">System.String</span></span>

### <span data-ttu-id="6ba04-152">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ba04-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ba04-153">출력</span><span class="sxs-lookup"><span data-stu-id="6ba04-153">OUTPUTS</span></span>

### <span data-ttu-id="6ba04-154">WindowsAzure. ResourceModel를 AzureStorageContainer로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba04-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="6ba04-155">상속자</span><span class="sxs-lookup"><span data-stu-id="6ba04-155">NOTES</span></span>

## <span data-ttu-id="6ba04-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ba04-156">RELATED LINKS</span></span>

[<span data-ttu-id="6ba04-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6ba04-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="6ba04-158">제거-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6ba04-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="6ba04-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6ba04-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


