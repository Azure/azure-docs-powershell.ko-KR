---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043137"
---
# <span data-ttu-id="bb254-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bb254-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="bb254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb254-102">SYNOPSIS</span></span>
<span data-ttu-id="bb254-103">Azure 저장소 blob에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="bb254-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb254-104">SYNTAX</span></span>

### <span data-ttu-id="bb254-105">BlobNameWithPermission (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb254-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb254-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="bb254-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb254-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="bb254-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb254-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="bb254-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb254-109">설명은</span><span class="sxs-lookup"><span data-stu-id="bb254-109">DESCRIPTION</span></span>
<span data-ttu-id="bb254-110">**AzStorageBlobSASToken** Cmdlet은 Azure storage blob에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="bb254-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bb254-111">EXAMPLES</span></span>

### <span data-ttu-id="bb254-112">예제 1: full blob 권한을 사용 하 여 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="bb254-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="bb254-113">이 예제에서는 full blob 권한이 있는 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="bb254-114">예제 2: 수명 기간 동안 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="bb254-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="bb254-115">이 예제에서는 수명 기간 동안 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="bb254-116">예제 3: OAuth 인증을 기반으로 하는 저장소 컨텍스트를 사용 하 여 사용자 Id SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="bb254-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="bb254-117">이 예제에서는 OAuth 인증을 기반으로 하는 저장소 컨텍스트를 사용 하 여 사용자 Id blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="bb254-118">변수</span><span class="sxs-lookup"><span data-stu-id="bb254-118">PARAMETERS</span></span>

### <span data-ttu-id="bb254-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="bb254-119">-Blob</span></span>
<span data-ttu-id="bb254-120">저장소 blob 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="bb254-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bb254-121">-CloudBlob</span></span>
<span data-ttu-id="bb254-122">**CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="bb254-123">**CloudBlob** 개체를 얻으려면 [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="bb254-124">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="bb254-124">-Container</span></span>
<span data-ttu-id="bb254-125">저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-125">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="bb254-126">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bb254-126">-Context</span></span>
<span data-ttu-id="bb254-127">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-127">Specifies the storage context.</span></span>
<span data-ttu-id="bb254-128">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 사용자 Id blob SAS 토큰이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="bb254-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb254-129">-DefaultProfile</span></span>
<span data-ttu-id="bb254-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb254-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bb254-131">-ExpiryTime</span></span>
<span data-ttu-id="bb254-132">공유 액세스 서명이 만료 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="bb254-133">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 만료 시간은 현재 시간에서 7 일 이내 여야 하며 현재 시간 보다 이전이 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="bb254-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="bb254-134">-FullUri</span></span>
<span data-ttu-id="bb254-135">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="bb254-136">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bb254-136">-IPAddressOrRange</span></span>
<span data-ttu-id="bb254-137">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="bb254-138">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="bb254-139">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="bb254-139">-Permission</span></span>
<span data-ttu-id="bb254-140">저장소 blob에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="bb254-141">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="bb254-142">-정책</span><span class="sxs-lookup"><span data-stu-id="bb254-142">-Policy</span></span>
<span data-ttu-id="bb254-143">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-143">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="bb254-144">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="bb254-144">-Protocol</span></span>
<span data-ttu-id="bb254-145">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="bb254-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="bb254-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="bb254-147">HttpsOnly</span></span>
* <span data-ttu-id="bb254-148">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="bb254-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bb254-149">-StartTime</span></span>
<span data-ttu-id="bb254-150">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="bb254-151">-확인</span><span class="sxs-lookup"><span data-stu-id="bb254-151">-Confirm</span></span>
<span data-ttu-id="bb254-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb254-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb254-153">-WhatIf</span></span>
<span data-ttu-id="bb254-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb254-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb254-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb254-156">CommonParameters</span></span>
<span data-ttu-id="bb254-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb254-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb254-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb254-159">입력</span><span class="sxs-lookup"><span data-stu-id="bb254-159">INPUTS</span></span>

### <span data-ttu-id="bb254-160">CloudBlob를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb254-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="bb254-161">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bb254-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bb254-162">출력</span><span class="sxs-lookup"><span data-stu-id="bb254-162">OUTPUTS</span></span>

### <span data-ttu-id="bb254-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb254-163">System.String</span></span>

## <span data-ttu-id="bb254-164">상속자</span><span class="sxs-lookup"><span data-stu-id="bb254-164">NOTES</span></span>

## <span data-ttu-id="bb254-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb254-165">RELATED LINKS</span></span>

[<span data-ttu-id="bb254-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bb254-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="bb254-167">새로운 AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="bb254-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
