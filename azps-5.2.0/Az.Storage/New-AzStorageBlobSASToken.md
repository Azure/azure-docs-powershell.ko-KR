---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349514"
---
# <span data-ttu-id="46467-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="46467-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="46467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46467-102">SYNOPSIS</span></span>
<span data-ttu-id="46467-103">Azure Storage Blob에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="46467-104">구문</span><span class="sxs-lookup"><span data-stu-id="46467-104">SYNTAX</span></span>

### <span data-ttu-id="46467-105">BlobNameWithPermission(기본값)</span><span class="sxs-lookup"><span data-stu-id="46467-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46467-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="46467-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46467-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="46467-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46467-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="46467-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46467-109">설명</span><span class="sxs-lookup"><span data-stu-id="46467-109">DESCRIPTION</span></span>
<span data-ttu-id="46467-110">**New-AzStorageBlobSASToken** cmdlet은 Azure Storage Blob에 대한 SAS(공유 액세스 서명) 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="46467-111">예제</span><span class="sxs-lookup"><span data-stu-id="46467-111">EXAMPLES</span></span>

### <span data-ttu-id="46467-112">예제 1: 전체 Blob 권한이 있는 Blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="46467-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="46467-113">이 예제에서는 전체 Blob 권한이 있는 Blob SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="46467-114">예제 2: 수명이 있는 Blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="46467-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="46467-115">이 예제에서는 수명이 있는 Blob SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="46467-116">예제 3: OAuth 인증을 기반으로 저장소 컨텍스트를 사용하여 사용자 ID SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="46467-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="46467-117">이 예제에서는 OAuth 인증을 기반으로 저장소 컨텍스트를 사용하여 사용자 ID Blob SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="46467-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46467-118">PARAMETERS</span></span>

### <span data-ttu-id="46467-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="46467-119">-Blob</span></span>
<span data-ttu-id="46467-120">저장소 Blob 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-120">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46467-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="46467-121">-BlobBaseClient</span></span>
<span data-ttu-id="46467-122">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="46467-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46467-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="46467-123">-CloudBlob</span></span>
<span data-ttu-id="46467-124">**CloudBlob** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="46467-125">**CloudBlob 개체를 얻습니다.** [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46467-126">-Container</span><span class="sxs-lookup"><span data-stu-id="46467-126">-Container</span></span>
<span data-ttu-id="46467-127">저장소 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-127">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46467-128">-Context</span><span class="sxs-lookup"><span data-stu-id="46467-128">-Context</span></span>
<span data-ttu-id="46467-129">저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-129">Specifies the storage context.</span></span>
<span data-ttu-id="46467-130">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 사용자 ID Blob SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="46467-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46467-131">-DefaultProfile</span></span>
<span data-ttu-id="46467-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46467-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46467-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="46467-133">-ExpiryTime</span></span>
<span data-ttu-id="46467-134">공유 액세스 서명이 만료되는 경우를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="46467-135">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 만료 시간은 현재 시간에서 7일이 되어야 합니다. 현재 시간보다 이전이 아니어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46467-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="46467-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="46467-136">-FullUri</span></span>
<span data-ttu-id="46467-137">이 cmdlet이 전체 Blob URI 및 공유 액세스 서명 토큰을 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46467-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="46467-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="46467-138">-IPAddressOrRange</span></span>
<span data-ttu-id="46467-139">요청을 수락할 IP 주소 또는 IP 주소 범위를 지정합니다(예: 168.1.5.65 또는 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="46467-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="46467-140">범위는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="46467-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="46467-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="46467-141">-Permission</span></span>
<span data-ttu-id="46467-142">저장소 Blob에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="46467-143">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="46467-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46467-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="46467-144">-Policy</span></span>
<span data-ttu-id="46467-145">Azure 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-145">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46467-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="46467-146">-Protocol</span></span>
<span data-ttu-id="46467-147">요청에 허용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="46467-148">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="46467-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="46467-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="46467-149">HttpsOnly</span></span>
* <span data-ttu-id="46467-150">HttpsOrHttp 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="46467-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="46467-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="46467-151">-StartTime</span></span>
<span data-ttu-id="46467-152">공유 액세스 서명이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="46467-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46467-153">-Confirm</span></span>
<span data-ttu-id="46467-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46467-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46467-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46467-155">-WhatIf</span></span>
<span data-ttu-id="46467-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="46467-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46467-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46467-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46467-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46467-158">CommonParameters</span></span>
<span data-ttu-id="46467-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46467-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46467-160">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46467-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46467-161">입력</span><span class="sxs-lookup"><span data-stu-id="46467-161">INPUTS</span></span>

### <span data-ttu-id="46467-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="46467-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="46467-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46467-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="46467-164">출력</span><span class="sxs-lookup"><span data-stu-id="46467-164">OUTPUTS</span></span>

### <span data-ttu-id="46467-165">System.String</span><span class="sxs-lookup"><span data-stu-id="46467-165">System.String</span></span>

## <span data-ttu-id="46467-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46467-166">NOTES</span></span>

## <span data-ttu-id="46467-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46467-167">RELATED LINKS</span></span>

[<span data-ttu-id="46467-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="46467-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="46467-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="46467-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
