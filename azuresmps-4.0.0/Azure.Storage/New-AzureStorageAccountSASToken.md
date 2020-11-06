---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523991"
---
# <span data-ttu-id="742e1-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="742e1-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="742e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742e1-102">SYNOPSIS</span></span>
<span data-ttu-id="742e1-103">SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-103">Creates an SAS token.</span></span>

## <span data-ttu-id="742e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="742e1-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="742e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="742e1-105">DESCRIPTION</span></span>
<span data-ttu-id="742e1-106">**AzureStorageSASToken** Cmdlet은 Azure 저장소 계정에 대 한 sa (계정 수준 공유 액세스 서명) 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="742e1-107">SAS 토큰을 사용 하 여 여러 서비스에 대 한 사용 권한을 위임 하거나 개체 수준 SAS 토큰과 함께 사용할 수 없는 서비스에 대 한 사용 권한을 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="742e1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="742e1-108">EXAMPLES</span></span>

### <span data-ttu-id="742e1-109">예제 1: SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="742e1-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="742e1-110">이 명령은 모든 권한이 있는 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="742e1-111">예제 2: IP 주소 범위에 대 한 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="742e1-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="742e1-112">이 명령은 지정 된 IP 주소 범위의 HTTPS 전용 요청에 대 한 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="742e1-113">변수</span><span class="sxs-lookup"><span data-stu-id="742e1-113">PARAMETERS</span></span>

### <span data-ttu-id="742e1-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="742e1-114">-Context</span></span>
<span data-ttu-id="742e1-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="742e1-116">New-AzureStorageContext cmdlet을 사용 하 여 **Azurestoragecontext** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="742e1-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="742e1-117">-ExpiryTime</span></span>
<span data-ttu-id="742e1-118">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="742e1-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="742e1-119">-IPAddressOrRange</span></span>
<span data-ttu-id="742e1-120">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="742e1-121">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="742e1-122">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="742e1-122">-Permission</span></span>
<span data-ttu-id="742e1-123">저장소 계정에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="742e1-124">사용 권한은 지정 된 리소스 종류와 일치 하는 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="742e1-125">허용 되는 사용 권한 값에 대 한 자세한 내용은 계정 SA 만들기를 참조 하세요.https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="742e1-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="742e1-126">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="742e1-126">-Protocol</span></span>
<span data-ttu-id="742e1-127">계정 SA로 작성 된 요청에 허용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="742e1-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="742e1-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="742e1-129">HttpsOnly</span></span>
- <span data-ttu-id="742e1-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="742e1-130">HttpsOrHttp</span></span>

<span data-ttu-id="742e1-131">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="742e1-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="742e1-132">-ResourceType</span></span>
<span data-ttu-id="742e1-133">SAS 토큰과 함께 사용할 수 있는 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="742e1-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="742e1-135">않아야</span><span class="sxs-lookup"><span data-stu-id="742e1-135">None</span></span>
- <span data-ttu-id="742e1-136">Services</span><span class="sxs-lookup"><span data-stu-id="742e1-136">Service</span></span>
- <span data-ttu-id="742e1-137">컨트롤러</span><span class="sxs-lookup"><span data-stu-id="742e1-137">Container</span></span>
- <span data-ttu-id="742e1-138">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="742e1-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="742e1-139">-서비스</span><span class="sxs-lookup"><span data-stu-id="742e1-139">-Service</span></span>
<span data-ttu-id="742e1-140">서비스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-140">Specifies the service.</span></span>
<span data-ttu-id="742e1-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="742e1-142">않아야</span><span class="sxs-lookup"><span data-stu-id="742e1-142">None</span></span>
- <span data-ttu-id="742e1-143">블</span><span class="sxs-lookup"><span data-stu-id="742e1-143">Blob</span></span>
- <span data-ttu-id="742e1-144">파일</span><span class="sxs-lookup"><span data-stu-id="742e1-144">File</span></span>
- <span data-ttu-id="742e1-145">전담팀</span><span class="sxs-lookup"><span data-stu-id="742e1-145">Queue</span></span>
- <span data-ttu-id="742e1-146">테이블로</span><span class="sxs-lookup"><span data-stu-id="742e1-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="742e1-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="742e1-147">-StartTime</span></span>
<span data-ttu-id="742e1-148">SA가 유효 하 게 되는 **DateTime** 개체로 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="742e1-149">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="742e1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742e1-150">CommonParameters</span></span>
<span data-ttu-id="742e1-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="742e1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742e1-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742e1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742e1-153">입력</span><span class="sxs-lookup"><span data-stu-id="742e1-153">INPUTS</span></span>

## <span data-ttu-id="742e1-154">출력</span><span class="sxs-lookup"><span data-stu-id="742e1-154">OUTPUTS</span></span>

## <span data-ttu-id="742e1-155">상속자</span><span class="sxs-lookup"><span data-stu-id="742e1-155">NOTES</span></span>

## <span data-ttu-id="742e1-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="742e1-156">RELATED LINKS</span></span>

[<span data-ttu-id="742e1-157">새로운 AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="742e1-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="742e1-158">새로운 AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="742e1-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="742e1-159">새로운 AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="742e1-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="742e1-160">새로운 AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="742e1-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="742e1-161">새로운 AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="742e1-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="742e1-162">새로운 AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="742e1-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


