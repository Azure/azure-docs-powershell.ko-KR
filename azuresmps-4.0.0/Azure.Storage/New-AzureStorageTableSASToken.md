---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524188"
---
# <span data-ttu-id="8ec74-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="8ec74-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="8ec74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec74-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec74-103">Azure 저장소 테이블에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="8ec74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ec74-104">SYNTAX</span></span>

### <span data-ttu-id="8ec74-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="8ec74-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="8ec74-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="8ec74-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="8ec74-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8ec74-107">DESCRIPTION</span></span>
<span data-ttu-id="8ec74-108">**AzureStorageTableSASToken** Cmdlet은 Azure 저장소 테이블에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="8ec74-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8ec74-109">EXAMPLES</span></span>

### <span data-ttu-id="8ec74-110">예제 1: 테이블에 대 한 모든 권한이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="8ec74-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="8ec74-111">이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="8ec74-112">이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="8ec74-113">예제 2: 파티션 범위에 대 한 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="8ec74-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="8ec74-114">이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="8ec74-115">이 명령은 토큰을 *StartPartitionKey* 및 *EndPartitionKey* 매개 변수에서 지정 하는 범위로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="8ec74-116">예제 3: 테이블에 저장 된 액세스 정책이 있는 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="8ec74-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="8ec74-117">이 명령은 ContosoResources 이라는 테이블에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="8ec74-118">명령이 ClientPolicy01 이라는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="8ec74-119">변수</span><span class="sxs-lookup"><span data-stu-id="8ec74-119">PARAMETERS</span></span>

### <span data-ttu-id="8ec74-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="8ec74-120">-Context</span></span>
<span data-ttu-id="8ec74-121">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8ec74-122">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8ec74-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8ec74-123">-EndPartitionKey</span></span>
<span data-ttu-id="8ec74-124">이 cmdlet이 만드는 토큰의 범위 끝에 대 한 파티션 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8ec74-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="8ec74-125">-EndRowKey</span></span>
<span data-ttu-id="8ec74-126">이 cmdlet이 만드는 토큰에 대 한 범위의 끝에 대 한 행 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8ec74-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8ec74-127">-ExpiryTime</span></span>
<span data-ttu-id="8ec74-128">SAS 토큰이 만료 되는 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="8ec74-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8ec74-129">-FullUri</span></span>
<span data-ttu-id="8ec74-130">이 cmdlet이 SAS 토큰과 함께 전체 큐 URI를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="8ec74-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8ec74-131">-IPAddressOrRange</span></span>
<span data-ttu-id="8ec74-132">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8ec74-133">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="8ec74-134">-이름</span><span class="sxs-lookup"><span data-stu-id="8ec74-134">-Name</span></span>
<span data-ttu-id="8ec74-135">Azure 저장소 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="8ec74-136">이 cmdlet은이 매개 변수에서 지정 하는 테이블에 대 한 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ec74-137">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="8ec74-137">-Permission</span></span>
<span data-ttu-id="8ec74-138">Azure Storage 테이블에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="8ec74-139">-정책</span><span class="sxs-lookup"><span data-stu-id="8ec74-139">-Policy</span></span>
<span data-ttu-id="8ec74-140">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="8ec74-141">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="8ec74-141">-Protocol</span></span>
<span data-ttu-id="8ec74-142">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8ec74-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8ec74-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8ec74-144">HttpsOnly</span></span>
* <span data-ttu-id="8ec74-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="8ec74-145">HttpsOrHttp</span></span>

<span data-ttu-id="8ec74-146">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="8ec74-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8ec74-147">-StartPartitionKey</span></span>
<span data-ttu-id="8ec74-148">이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 파티션 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8ec74-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="8ec74-149">-StartRowKey</span></span>
<span data-ttu-id="8ec74-150">이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 행 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8ec74-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8ec74-151">-StartTime</span></span>
<span data-ttu-id="8ec74-152">SAS 토큰이 유효 하 게 되는 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="8ec74-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec74-153">CommonParameters</span></span>
<span data-ttu-id="8ec74-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec74-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec74-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec74-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec74-156">입력</span><span class="sxs-lookup"><span data-stu-id="8ec74-156">INPUTS</span></span>

## <span data-ttu-id="8ec74-157">출력</span><span class="sxs-lookup"><span data-stu-id="8ec74-157">OUTPUTS</span></span>

## <span data-ttu-id="8ec74-158">상속자</span><span class="sxs-lookup"><span data-stu-id="8ec74-158">NOTES</span></span>

## <span data-ttu-id="8ec74-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ec74-159">RELATED LINKS</span></span>

[<span data-ttu-id="8ec74-160">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ec74-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
