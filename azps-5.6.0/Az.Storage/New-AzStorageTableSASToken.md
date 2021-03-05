---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 65a90f703f142a01429fb215bd5c66bef74bb4c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008299"
---
# <span data-ttu-id="f8b1c-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="f8b1c-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="f8b1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b1c-103">Azure Storage 테이블에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="f8b1c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8b1c-104">SYNTAX</span></span>

### <span data-ttu-id="f8b1c-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f8b1c-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8b1c-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f8b1c-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b1c-107">설명</span><span class="sxs-lookup"><span data-stu-id="f8b1c-107">DESCRIPTION</span></span>
<span data-ttu-id="f8b1c-108">**New-AzStorageTableSASToken** cmdlet은 Azure Storage 테이블에 대한 SAS(공유 액세스 서명) 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="f8b1c-109">예제</span><span class="sxs-lookup"><span data-stu-id="f8b1c-109">EXAMPLES</span></span>

### <span data-ttu-id="f8b1c-110">예제 1: 테이블에 대한 전체 사용 권한이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="f8b1c-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="f8b1c-111">이 명령은 ContosoResources라는 테이블에 대한 전체 사용 권한이 있는 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="f8b1c-112">이 토큰은 읽기, 추가, 업데이트 및 삭제 권한을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="f8b1c-113">예제 2: 다양한 파티션에 대한 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="f8b1c-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="f8b1c-114">이 명령은 ContosoResources라는 테이블에 대한 전체 사용 권한이 있는 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="f8b1c-115">명령은 *StartPartitionKey* 및 *EndPartitionKey* 매개 변수가 지정하는 범위로 토큰을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="f8b1c-116">예제 3: 테이블에 대한 저장된 액세스 정책이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="f8b1c-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="f8b1c-117">이 명령은 ContosoResources라는 테이블에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="f8b1c-118">명령은 ClientPolicy01이라는 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="f8b1c-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8b1c-119">PARAMETERS</span></span>

### <span data-ttu-id="f8b1c-120">-Context</span><span class="sxs-lookup"><span data-stu-id="f8b1c-120">-Context</span></span>
<span data-ttu-id="f8b1c-121">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f8b1c-122">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f8b1c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b1c-123">-DefaultProfile</span></span>
<span data-ttu-id="f8b1c-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b1c-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="f8b1c-125">-EndPartitionKey</span></span>
<span data-ttu-id="f8b1c-126">이 cmdlet이 만드는 토큰에 대한 범위 끝의 파티션 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b1c-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="f8b1c-127">-EndRowKey</span></span>
<span data-ttu-id="f8b1c-128">이 cmdlet이 만드는 토큰에 대한 범위의 끝에 대한 행 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b1c-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f8b1c-129">-ExpiryTime</span></span>
<span data-ttu-id="f8b1c-130">SAS 토큰이 만료되는 경우를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="f8b1c-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f8b1c-131">-FullUri</span></span>
<span data-ttu-id="f8b1c-132">이 cmdlet은 SAS 토큰을 사용하여 전체 큐 URI를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="f8b1c-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f8b1c-133">-IPAddressOrRange</span></span>
<span data-ttu-id="f8b1c-134">168.1.5.65 또는 168.5.60-168.1.5.70과 같은 요청을 수락할 IP 주소 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f8b1c-135">범위는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="f8b1c-136">-Name</span><span class="sxs-lookup"><span data-stu-id="f8b1c-136">-Name</span></span>
<span data-ttu-id="f8b1c-137">Azure Storage 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="f8b1c-138">이 cmdlet은 이 매개 변수가 지정하는 테이블에 대한 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b1c-139">-권한</span><span class="sxs-lookup"><span data-stu-id="f8b1c-139">-Permission</span></span>
<span data-ttu-id="f8b1c-140">Azure Storage 테이블에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="f8b1c-141">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f8b1c-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="f8b1c-142">-Policy</span></span>
<span data-ttu-id="f8b1c-143">이 SAS 토큰에 대한 사용 권한을 포함하는 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="f8b1c-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f8b1c-144">-Protocol</span></span>
<span data-ttu-id="f8b1c-145">요청에 대해 허용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f8b1c-146">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f8b1c-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f8b1c-147">HttpsOnly</span></span>
* <span data-ttu-id="f8b1c-148">HttpsOrHttp 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b1c-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="f8b1c-149">-StartPartitionKey</span></span>
<span data-ttu-id="f8b1c-150">이 cmdlet이 만드는 토큰에 대한 범위의 시작 부분의 파티션 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b1c-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="f8b1c-151">-StartRowKey</span></span>
<span data-ttu-id="f8b1c-152">이 cmdlet이 만드는 토큰에 대한 범위의 시작에 대한 행 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b1c-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f8b1c-153">-StartTime</span></span>
<span data-ttu-id="f8b1c-154">SAS 토큰이 유효한 경우를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="f8b1c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b1c-155">CommonParameters</span></span>
<span data-ttu-id="f8b1c-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b1c-157">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f8b1c-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b1c-158">입력</span><span class="sxs-lookup"><span data-stu-id="f8b1c-158">INPUTS</span></span>

### <span data-ttu-id="f8b1c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="f8b1c-159">System.String</span></span>

### <span data-ttu-id="f8b1c-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8b1c-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f8b1c-161">출력</span><span class="sxs-lookup"><span data-stu-id="f8b1c-161">OUTPUTS</span></span>

### <span data-ttu-id="f8b1c-162">System.String</span><span class="sxs-lookup"><span data-stu-id="f8b1c-162">System.String</span></span>

## <span data-ttu-id="f8b1c-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8b1c-163">NOTES</span></span>

## <span data-ttu-id="f8b1c-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8b1c-164">RELATED LINKS</span></span>

[<span data-ttu-id="f8b1c-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8b1c-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
