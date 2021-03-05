---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002608"
---
# <span data-ttu-id="cd6a5-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="cd6a5-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="cd6a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6a5-103">계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="cd6a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd6a5-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd6a5-105">설명</span><span class="sxs-lookup"><span data-stu-id="cd6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="cd6a5-106">**New-AzStorageSASToken** cmdlet은 Azure Storage 계정에 대한 SAS(계정 수준 공유 액세스 서명) 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="cd6a5-107">SAS 토큰을 사용하여 여러 서비스에 대한 권한을 위임하거나 개체 수준 SAS 토큰으로 사용할 수 없는 서비스에 대한 권한을 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="cd6a5-108">예제</span><span class="sxs-lookup"><span data-stu-id="cd6a5-108">EXAMPLES</span></span>

### <span data-ttu-id="cd6a5-109">예제 1: 전체 권한이 있는 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="cd6a5-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="cd6a5-110">이 명령은 전체 권한이 있는 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="cd6a5-111">예제 2: 다양한 IP 주소에 대한 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="cd6a5-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="cd6a5-112">이 명령은 지정된 IP 주소 범위에서 HTTPS 전용 요청에 대한 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="cd6a5-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd6a5-113">PARAMETERS</span></span>

### <span data-ttu-id="cd6a5-114">-Context</span><span class="sxs-lookup"><span data-stu-id="cd6a5-114">-Context</span></span>
<span data-ttu-id="cd6a5-115">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cd6a5-116">**azureStorageContext** 개체를 New-AzStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="cd6a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6a5-117">-DefaultProfile</span></span>
<span data-ttu-id="cd6a5-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd6a5-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cd6a5-119">-ExpiryTime</span></span>
<span data-ttu-id="cd6a5-120">공유 액세스 서명이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a5-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cd6a5-121">-IPAddressOrRange</span></span>
<span data-ttu-id="cd6a5-122">168.1.5.65 또는 168.5.60-168.1.5.70과 같은 요청을 수락할 IP 주소 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="cd6a5-123">범위는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-123">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a5-124">-권한</span><span class="sxs-lookup"><span data-stu-id="cd6a5-124">-Permission</span></span>
<span data-ttu-id="cd6a5-125">Storage 계정에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="cd6a5-126">사용 권한은 지정된 리소스 유형과 일치하는 경우만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="cd6a5-127">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="cd6a5-128">허용되는 사용 권한 값에 대한 자세한 내용은 계정 SAS 생성을 참조하세요. http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="cd6a5-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a5-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cd6a5-129">-Protocol</span></span>
<span data-ttu-id="cd6a5-130">계정 SAS로 만든 요청에 대해 허용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="cd6a5-131">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd6a5-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="cd6a5-132">HttpsOnly</span></span>
- <span data-ttu-id="cd6a5-133">HttpsOrHttp 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a5-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cd6a5-134">-ResourceType</span></span>
<span data-ttu-id="cd6a5-135">SAS 토큰에서 사용할 수 있는 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="cd6a5-136">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd6a5-137">없음</span><span class="sxs-lookup"><span data-stu-id="cd6a5-137">None</span></span>
- <span data-ttu-id="cd6a5-138">서비스</span><span class="sxs-lookup"><span data-stu-id="cd6a5-138">Service</span></span>
- <span data-ttu-id="cd6a5-139">컨테이너</span><span class="sxs-lookup"><span data-stu-id="cd6a5-139">Container</span></span>
- <span data-ttu-id="cd6a5-140">개체</span><span class="sxs-lookup"><span data-stu-id="cd6a5-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a5-141">-Service</span><span class="sxs-lookup"><span data-stu-id="cd6a5-141">-Service</span></span>
<span data-ttu-id="cd6a5-142">서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-142">Specifies the service.</span></span>
<span data-ttu-id="cd6a5-143">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd6a5-144">없음</span><span class="sxs-lookup"><span data-stu-id="cd6a5-144">None</span></span>
- <span data-ttu-id="cd6a5-145">Blob</span><span class="sxs-lookup"><span data-stu-id="cd6a5-145">Blob</span></span>
- <span data-ttu-id="cd6a5-146">파일</span><span class="sxs-lookup"><span data-stu-id="cd6a5-146">File</span></span>
- <span data-ttu-id="cd6a5-147">큐</span><span class="sxs-lookup"><span data-stu-id="cd6a5-147">Queue</span></span>
- <span data-ttu-id="cd6a5-148">표</span><span class="sxs-lookup"><span data-stu-id="cd6a5-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a5-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cd6a5-149">-StartTime</span></span>
<span data-ttu-id="cd6a5-150">SAS가 유효한 날짜 **시간** 개체로 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="cd6a5-151">DateTime 개체를 **얻은** 경우 Get-Date cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6a5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6a5-152">CommonParameters</span></span>
<span data-ttu-id="cd6a5-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6a5-154">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6a5-155">입력</span><span class="sxs-lookup"><span data-stu-id="cd6a5-155">INPUTS</span></span>

### <span data-ttu-id="cd6a5-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd6a5-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cd6a5-157">출력</span><span class="sxs-lookup"><span data-stu-id="cd6a5-157">OUTPUTS</span></span>

### <span data-ttu-id="cd6a5-158">System.String</span><span class="sxs-lookup"><span data-stu-id="cd6a5-158">System.String</span></span>

## <span data-ttu-id="cd6a5-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd6a5-159">NOTES</span></span>

## <span data-ttu-id="cd6a5-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd6a5-160">RELATED LINKS</span></span>

[<span data-ttu-id="cd6a5-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cd6a5-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="cd6a5-162">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cd6a5-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="cd6a5-163">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="cd6a5-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="cd6a5-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="cd6a5-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="cd6a5-165">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="cd6a5-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="cd6a5-166">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="cd6a5-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


