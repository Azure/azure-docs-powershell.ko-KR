---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188841"
---
# <span data-ttu-id="7aba2-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="7aba2-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="7aba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aba2-102">SYNOPSIS</span></span>
<span data-ttu-id="7aba2-103">공유에 대한 저장소 용량을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="7aba2-104">구문</span><span class="sxs-lookup"><span data-stu-id="7aba2-104">SYNTAX</span></span>

### <span data-ttu-id="7aba2-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7aba2-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7aba2-106">공유</span><span class="sxs-lookup"><span data-stu-id="7aba2-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="7aba2-107">설명</span><span class="sxs-lookup"><span data-stu-id="7aba2-107">DESCRIPTION</span></span>
<span data-ttu-id="7aba2-108">**Set-AzStorageShareQuota** cmdlet은 지정된 공유에 대한 저장소 용량을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="7aba2-109">예제</span><span class="sxs-lookup"><span data-stu-id="7aba2-109">EXAMPLES</span></span>

### <span data-ttu-id="7aba2-110">예제 1: 공유의 저장소 용량 설정</span><span class="sxs-lookup"><span data-stu-id="7aba2-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="7aba2-111">이 명령은 ContosoShare01이라는 공유에 대한 저장소 용량을 1024GB로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="7aba2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7aba2-112">PARAMETERS</span></span>

### <span data-ttu-id="7aba2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7aba2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7aba2-114">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7aba2-115">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7aba2-116">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7aba2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7aba2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7aba2-118">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7aba2-119">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7aba2-120">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7aba2-121">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7aba2-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="7aba2-123">-Context</span><span class="sxs-lookup"><span data-stu-id="7aba2-123">-Context</span></span>
<span data-ttu-id="7aba2-124">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7aba2-125">저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aba2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aba2-126">-DefaultProfile</span></span>
<span data-ttu-id="7aba2-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aba2-128">-할당량</span><span class="sxs-lookup"><span data-stu-id="7aba2-128">-Quota</span></span>
<span data-ttu-id="7aba2-129">할당량 값을 기가바이트(GB)로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="7aba2-130">에서 할당량 제한을 https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aba2-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7aba2-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7aba2-132">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7aba2-133">-공유</span><span class="sxs-lookup"><span data-stu-id="7aba2-133">-Share</span></span>
<span data-ttu-id="7aba2-134">이 cmdlet이 할당량을 설정하는 공유를 나타내는 **CloudFileShare** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="7aba2-135">**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aba2-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7aba2-136">-ShareName</span></span>
<span data-ttu-id="7aba2-137">할당량 설정에 사용할 파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aba2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aba2-138">CommonParameters</span></span>
<span data-ttu-id="7aba2-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7aba2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aba2-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7aba2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aba2-141">입력</span><span class="sxs-lookup"><span data-stu-id="7aba2-141">INPUTS</span></span>

### <span data-ttu-id="7aba2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7aba2-142">System.String</span></span>

### <span data-ttu-id="7aba2-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7aba2-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="7aba2-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7aba2-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7aba2-145">출력</span><span class="sxs-lookup"><span data-stu-id="7aba2-145">OUTPUTS</span></span>

### <span data-ttu-id="7aba2-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="7aba2-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="7aba2-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7aba2-147">NOTES</span></span>

## <span data-ttu-id="7aba2-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7aba2-148">RELATED LINKS</span></span>

[<span data-ttu-id="7aba2-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7aba2-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="7aba2-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="7aba2-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="7aba2-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7aba2-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
