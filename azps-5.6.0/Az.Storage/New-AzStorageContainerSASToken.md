---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 09cbfb953118e5d6e29f2af25cd4653939135f07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002507"
---
# <span data-ttu-id="bece0-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="bece0-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="bece0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bece0-102">SYNOPSIS</span></span>
<span data-ttu-id="bece0-103">Azure 저장소 컨테이너에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="bece0-104">구문</span><span class="sxs-lookup"><span data-stu-id="bece0-104">SYNTAX</span></span>

### <span data-ttu-id="bece0-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="bece0-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bece0-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="bece0-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bece0-107">설명</span><span class="sxs-lookup"><span data-stu-id="bece0-107">DESCRIPTION</span></span>
<span data-ttu-id="bece0-108">**New-AzStorageContainerSASToken** cmdlet은 Azure 저장소 컨테이너에 대한 SAS(공유 액세스 서명) 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="bece0-109">예제</span><span class="sxs-lookup"><span data-stu-id="bece0-109">EXAMPLES</span></span>

### <span data-ttu-id="bece0-110">예제 1: 전체 컨테이너 사용 권한이 있는 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="bece0-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="bece0-111">이 예제에서는 전체 컨테이너 권한이 있는 컨테이너 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="bece0-112">예제 2: 파이프라인에 의해 여러 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="bece0-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="bece0-113">이 예제에서는 파이프라인을 사용하여 여러 컨테이너 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="bece0-114">예제 3: 공유 액세스 정책으로 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="bece0-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="bece0-115">이 예제에서는 공유 액세스 정책이 있는 컨테이너 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="bece0-116">예제 3: OAuth 인증을 기반으로 저장소 컨텍스트를 사용하여 사용자 ID 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="bece0-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="bece0-117">이 예제에서는 OAuth 인증을 기반으로 저장소 컨텍스트가 있는 사용자 ID 컨테이너 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="bece0-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bece0-118">PARAMETERS</span></span>

### <span data-ttu-id="bece0-119">-Context</span><span class="sxs-lookup"><span data-stu-id="bece0-119">-Context</span></span>
<span data-ttu-id="bece0-120">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bece0-121">New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="bece0-122">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 사용자 ID 컨테이너 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="bece0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bece0-123">-DefaultProfile</span></span>
<span data-ttu-id="bece0-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bece0-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bece0-125">-ExpiryTime</span></span>
<span data-ttu-id="bece0-126">공유 액세스 서명이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="bece0-127">사용자가 시작 시간을 설정하지만 만료 시간이 아닌 경우 만료 시간은 시작 시간과 1시간으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="bece0-128">시작 시간이나 만료 시간이 지정되지 않은 경우 만료 시간은 현재 시간과 1시간으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="bece0-129">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 만료 시간은 현재 시간에서 7일이 되어야 합니다. 현재 시간보다 더 일찍 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="bece0-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="bece0-130">-FullUri</span></span>
<span data-ttu-id="bece0-131">이 cmdlet은 전체 Blob URI 및 공유 액세스 서명 토큰을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="bece0-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bece0-132">-IPAddressOrRange</span></span>
<span data-ttu-id="bece0-133">168.1.5.65 또는 168.5.60-168.1.5.70과 같은 요청을 수락할 IP 주소 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="bece0-134">범위는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="bece0-135">-Name</span><span class="sxs-lookup"><span data-stu-id="bece0-135">-Name</span></span>
<span data-ttu-id="bece0-136">Azure Storage 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-136">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="bece0-137">-권한</span><span class="sxs-lookup"><span data-stu-id="bece0-137">-Permission</span></span>
<span data-ttu-id="bece0-138">저장소 컨테이너에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="bece0-139">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bece0-140">-Policy</span><span class="sxs-lookup"><span data-stu-id="bece0-140">-Policy</span></span>
<span data-ttu-id="bece0-141">Azure 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-141">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bece0-142">-Protocol</span><span class="sxs-lookup"><span data-stu-id="bece0-142">-Protocol</span></span>
<span data-ttu-id="bece0-143">요청에 대해 허용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="bece0-144">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="bece0-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="bece0-145">HttpsOnly</span></span>
* <span data-ttu-id="bece0-146">HttpsOrHttp 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="bece0-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bece0-147">-StartTime</span></span>
<span data-ttu-id="bece0-148">공유 액세스 서명이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="bece0-149">-확인</span><span class="sxs-lookup"><span data-stu-id="bece0-149">-Confirm</span></span>
<span data-ttu-id="bece0-150">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bece0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bece0-151">-WhatIf</span></span>
<span data-ttu-id="bece0-152">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bece0-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bece0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bece0-154">CommonParameters</span></span>
<span data-ttu-id="bece0-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bece0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bece0-156">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bece0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bece0-157">입력</span><span class="sxs-lookup"><span data-stu-id="bece0-157">INPUTS</span></span>

### <span data-ttu-id="bece0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="bece0-158">System.String</span></span>

### <span data-ttu-id="bece0-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bece0-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bece0-160">출력</span><span class="sxs-lookup"><span data-stu-id="bece0-160">OUTPUTS</span></span>

### <span data-ttu-id="bece0-161">System.String</span><span class="sxs-lookup"><span data-stu-id="bece0-161">System.String</span></span>

## <span data-ttu-id="bece0-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bece0-162">NOTES</span></span>

## <span data-ttu-id="bece0-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bece0-163">RELATED LINKS</span></span>

[<span data-ttu-id="bece0-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bece0-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
