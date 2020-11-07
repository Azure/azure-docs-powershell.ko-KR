---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 739cd5b12cfc33abb57e4e04d2834b195966b126
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711792"
---
# <span data-ttu-id="e8a23-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="e8a23-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="e8a23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a23-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a23-103">Azure 저장소 테이블에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8a23-104">SYNTAX</span></span>

### <span data-ttu-id="e8a23-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="e8a23-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e8a23-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="e8a23-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e8a23-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e8a23-107">DESCRIPTION</span></span>
<span data-ttu-id="e8a23-108">**AzureStorageTableSASToken** Cmdlet은 Azure 저장소 테이블에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="e8a23-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e8a23-109">EXAMPLES</span></span>

### <span data-ttu-id="e8a23-110">예제 1: 테이블에 대 한 모든 권한이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="e8a23-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="e8a23-111">이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="e8a23-112">이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="e8a23-113">예제 2: 파티션 범위에 대 한 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="e8a23-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="e8a23-114">이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="e8a23-115">이 명령은 토큰을 *StartPartitionKey* 및 *EndPartitionKey* 매개 변수에서 지정 하는 범위로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="e8a23-116">예제 3: 테이블에 저장 된 액세스 정책이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="e8a23-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="e8a23-117">이 명령은 ContosoResources 이라는 테이블에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="e8a23-118">명령이 ClientPolicy01 이라는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="e8a23-119">변수</span><span class="sxs-lookup"><span data-stu-id="e8a23-119">PARAMETERS</span></span>

### <span data-ttu-id="e8a23-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e8a23-120">-Context</span></span>
<span data-ttu-id="e8a23-121">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e8a23-122">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="e8a23-123">-EndPartitionKey</span></span>
<span data-ttu-id="e8a23-124">이 cmdlet이 만드는 토큰의 범위 끝에 대 한 파티션 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="e8a23-125">-EndRowKey</span></span>
<span data-ttu-id="e8a23-126">이 cmdlet이 만드는 토큰에 대 한 범위의 끝에 대 한 행 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e8a23-127">-ExpiryTime</span></span>
<span data-ttu-id="e8a23-128">SAS 토큰이 만료 되는 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-128">Specifies when the SAS token expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e8a23-129">-FullUri</span></span>
<span data-ttu-id="e8a23-130">이 cmdlet이 SAS 토큰과 함께 전체 큐 URI를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e8a23-131">-IPAddressOrRange</span></span>
<span data-ttu-id="e8a23-132">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e8a23-133">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-133">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-134">-이름</span><span class="sxs-lookup"><span data-stu-id="e8a23-134">-Name</span></span>
<span data-ttu-id="e8a23-135">Azure 저장소 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="e8a23-136">이 cmdlet은이 매개 변수에서 지정 하는 테이블에 대 한 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-137">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="e8a23-137">-Permission</span></span>
<span data-ttu-id="e8a23-138">Azure Storage 테이블에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-138">Specifies permissions for an Azure Storage table.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-139">-정책</span><span class="sxs-lookup"><span data-stu-id="e8a23-139">-Policy</span></span>
<span data-ttu-id="e8a23-140">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-141">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="e8a23-141">-Protocol</span></span>
<span data-ttu-id="e8a23-142">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e8a23-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e8a23-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e8a23-144">HttpsOnly</span></span>
* <span data-ttu-id="e8a23-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e8a23-145">HttpsOrHttp</span></span>

<span data-ttu-id="e8a23-146">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-146">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="e8a23-147">-StartPartitionKey</span></span>
<span data-ttu-id="e8a23-148">이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 파티션 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="e8a23-149">-StartRowKey</span></span>
<span data-ttu-id="e8a23-150">이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 행 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e8a23-151">-StartTime</span></span>
<span data-ttu-id="e8a23-152">SAS 토큰이 유효 하 게 되는 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-152">Specifies when the SAS token becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a23-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a23-153">CommonParameters</span></span>
<span data-ttu-id="e8a23-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a23-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8a23-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a23-156">입력</span><span class="sxs-lookup"><span data-stu-id="e8a23-156">INPUTS</span></span>

### <span data-ttu-id="e8a23-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e8a23-157">IStorageContext</span></span>

<span data-ttu-id="e8a23-158">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e8a23-159">이름</span><span class="sxs-lookup"><span data-stu-id="e8a23-159">String</span></span>

<span data-ttu-id="e8a23-160">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a23-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e8a23-161">출력</span><span class="sxs-lookup"><span data-stu-id="e8a23-161">OUTPUTS</span></span>

### <span data-ttu-id="e8a23-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e8a23-162">System.String</span></span>

## <span data-ttu-id="e8a23-163">상속자</span><span class="sxs-lookup"><span data-stu-id="e8a23-163">NOTES</span></span>

## <span data-ttu-id="e8a23-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8a23-164">RELATED LINKS</span></span>

[<span data-ttu-id="e8a23-165">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e8a23-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
