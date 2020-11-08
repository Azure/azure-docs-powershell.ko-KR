---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217173"
---
# <span data-ttu-id="df59a-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="df59a-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="df59a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df59a-102">SYNOPSIS</span></span>
<span data-ttu-id="df59a-103">Azure 저장소 blob에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="df59a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="df59a-104">SYNTAX</span></span>

### <span data-ttu-id="df59a-105">BlobNameWithPermission (기본값)</span><span class="sxs-lookup"><span data-stu-id="df59a-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df59a-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="df59a-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df59a-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="df59a-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df59a-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="df59a-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df59a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="df59a-109">DESCRIPTION</span></span>
<span data-ttu-id="df59a-110">**AzStorageBlobSASToken** Cmdlet은 Azure storage blob에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="df59a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="df59a-111">EXAMPLES</span></span>

### <span data-ttu-id="df59a-112">예제 1: full blob 권한을 사용 하 여 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="df59a-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="df59a-113">이 예제에서는 full blob 권한이 있는 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="df59a-114">예제 2: 수명 기간 동안 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="df59a-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="df59a-115">이 예제에서는 수명 기간 동안 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="df59a-116">예제 3: OAuth 인증을 기반으로 하는 저장소 컨텍스트를 사용 하 여 사용자 Id SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="df59a-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="df59a-117">이 예제에서는 OAuth 인증을 기반으로 하는 저장소 컨텍스트를 사용 하 여 사용자 Id blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="df59a-118">변수</span><span class="sxs-lookup"><span data-stu-id="df59a-118">PARAMETERS</span></span>

### <span data-ttu-id="df59a-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="df59a-119">-Blob</span></span>
<span data-ttu-id="df59a-120">저장소 blob 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="df59a-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="df59a-121">-BlobBaseClient</span></span>
<span data-ttu-id="df59a-122">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="df59a-122">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="df59a-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="df59a-123">-CloudBlob</span></span>
<span data-ttu-id="df59a-124">**CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="df59a-125">**CloudBlob** 개체를 얻으려면 [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="df59a-126">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="df59a-126">-Container</span></span>
<span data-ttu-id="df59a-127">저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="df59a-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="df59a-128">-Context</span></span>
<span data-ttu-id="df59a-129">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-129">Specifies the storage context.</span></span>
<span data-ttu-id="df59a-130">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 사용자 Id blob SAS 토큰이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="df59a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df59a-131">-DefaultProfile</span></span>
<span data-ttu-id="df59a-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df59a-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="df59a-133">-ExpiryTime</span></span>
<span data-ttu-id="df59a-134">공유 액세스 서명이 만료 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="df59a-135">저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 만료 시간은 현재 시간에서 7 일 이내 여야 하며 현재 시간 보다 이전이 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="df59a-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="df59a-136">-FullUri</span></span>
<span data-ttu-id="df59a-137">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="df59a-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="df59a-138">-IPAddressOrRange</span></span>
<span data-ttu-id="df59a-139">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="df59a-140">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="df59a-141">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="df59a-141">-Permission</span></span>
<span data-ttu-id="df59a-142">저장소 blob에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="df59a-143">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="df59a-144">-정책</span><span class="sxs-lookup"><span data-stu-id="df59a-144">-Policy</span></span>
<span data-ttu-id="df59a-145">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="df59a-146">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="df59a-146">-Protocol</span></span>
<span data-ttu-id="df59a-147">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="df59a-148">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="df59a-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="df59a-149">HttpsOnly</span></span>
* <span data-ttu-id="df59a-150">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="df59a-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="df59a-151">-StartTime</span></span>
<span data-ttu-id="df59a-152">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="df59a-153">-확인</span><span class="sxs-lookup"><span data-stu-id="df59a-153">-Confirm</span></span>
<span data-ttu-id="df59a-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df59a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df59a-155">-WhatIf</span></span>
<span data-ttu-id="df59a-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df59a-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df59a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df59a-158">CommonParameters</span></span>
<span data-ttu-id="df59a-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df59a-160">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df59a-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df59a-161">입력</span><span class="sxs-lookup"><span data-stu-id="df59a-161">INPUTS</span></span>

### <span data-ttu-id="df59a-162">CloudBlob를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df59a-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="df59a-163">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="df59a-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df59a-164">출력</span><span class="sxs-lookup"><span data-stu-id="df59a-164">OUTPUTS</span></span>

### <span data-ttu-id="df59a-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="df59a-165">System.String</span></span>

## <span data-ttu-id="df59a-166">상속자</span><span class="sxs-lookup"><span data-stu-id="df59a-166">NOTES</span></span>

## <span data-ttu-id="df59a-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df59a-167">RELATED LINKS</span></span>

[<span data-ttu-id="df59a-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="df59a-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="df59a-169">새로운 AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="df59a-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
