---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 743baee44cc038dd54ab2a09d4362848e3d4c9a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874256"
---
# <span data-ttu-id="7fd2b-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="7fd2b-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="7fd2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd2b-103">Azure 저장소 테이블에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="7fd2b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fd2b-104">SYNTAX</span></span>

### <span data-ttu-id="7fd2b-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd2b-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fd2b-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="7fd2b-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fd2b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7fd2b-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd2b-108">**AzStorageTableSASToken** Cmdlet은 Azure 저장소 테이블에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="7fd2b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7fd2b-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd2b-110">예제 1: 테이블에 대 한 모든 권한이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="7fd2b-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="7fd2b-111">이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="7fd2b-112">이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="7fd2b-113">예제 2: 파티션 범위에 대 한 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="7fd2b-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="7fd2b-114">이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="7fd2b-115">이 명령은 토큰을 *StartPartitionKey* 및 *EndPartitionKey* 매개 변수에서 지정 하는 범위로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="7fd2b-116">예제 3: 테이블에 저장 된 액세스 정책이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="7fd2b-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="7fd2b-117">이 명령은 ContosoResources 이라는 테이블에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="7fd2b-118">명령이 ClientPolicy01 이라는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="7fd2b-119">변수</span><span class="sxs-lookup"><span data-stu-id="7fd2b-119">PARAMETERS</span></span>

### <span data-ttu-id="7fd2b-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7fd2b-120">-Context</span></span>
<span data-ttu-id="7fd2b-121">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7fd2b-122">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7fd2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd2b-123">-DefaultProfile</span></span>
<span data-ttu-id="7fd2b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd2b-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="7fd2b-125">-EndPartitionKey</span></span>
<span data-ttu-id="7fd2b-126">이 cmdlet이 만드는 토큰의 범위 끝에 대 한 파티션 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7fd2b-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="7fd2b-127">-EndRowKey</span></span>
<span data-ttu-id="7fd2b-128">이 cmdlet이 만드는 토큰에 대 한 범위의 끝에 대 한 행 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7fd2b-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7fd2b-129">-ExpiryTime</span></span>
<span data-ttu-id="7fd2b-130">SAS 토큰이 만료 되는 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="7fd2b-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="7fd2b-131">-FullUri</span></span>
<span data-ttu-id="7fd2b-132">이 cmdlet이 SAS 토큰과 함께 전체 큐 URI를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="7fd2b-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7fd2b-133">-IPAddressOrRange</span></span>
<span data-ttu-id="7fd2b-134">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="7fd2b-135">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="7fd2b-136">-이름</span><span class="sxs-lookup"><span data-stu-id="7fd2b-136">-Name</span></span>
<span data-ttu-id="7fd2b-137">Azure 저장소 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="7fd2b-138">이 cmdlet은이 매개 변수에서 지정 하는 테이블에 대 한 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="7fd2b-139">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="7fd2b-139">-Permission</span></span>
<span data-ttu-id="7fd2b-140">Azure Storage 테이블에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="7fd2b-141">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7fd2b-142">-정책</span><span class="sxs-lookup"><span data-stu-id="7fd2b-142">-Policy</span></span>
<span data-ttu-id="7fd2b-143">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="7fd2b-144">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7fd2b-144">-Protocol</span></span>
<span data-ttu-id="7fd2b-145">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="7fd2b-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="7fd2b-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7fd2b-147">HttpsOnly</span></span>
* <span data-ttu-id="7fd2b-148">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="7fd2b-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="7fd2b-149">-StartPartitionKey</span></span>
<span data-ttu-id="7fd2b-150">이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 파티션 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7fd2b-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="7fd2b-151">-StartRowKey</span></span>
<span data-ttu-id="7fd2b-152">이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 행 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7fd2b-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7fd2b-153">-StartTime</span></span>
<span data-ttu-id="7fd2b-154">SAS 토큰이 유효 하 게 되는 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="7fd2b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd2b-155">CommonParameters</span></span>
<span data-ttu-id="7fd2b-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd2b-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd2b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd2b-158">입력</span><span class="sxs-lookup"><span data-stu-id="7fd2b-158">INPUTS</span></span>

### <span data-ttu-id="7fd2b-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7fd2b-159">System.String</span></span>

### <span data-ttu-id="7fd2b-160">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fd2b-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7fd2b-161">출력</span><span class="sxs-lookup"><span data-stu-id="7fd2b-161">OUTPUTS</span></span>

### <span data-ttu-id="7fd2b-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7fd2b-162">System.String</span></span>

## <span data-ttu-id="7fd2b-163">상속자</span><span class="sxs-lookup"><span data-stu-id="7fd2b-163">NOTES</span></span>

## <span data-ttu-id="7fd2b-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fd2b-164">RELATED LINKS</span></span>

[<span data-ttu-id="7fd2b-165">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fd2b-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
