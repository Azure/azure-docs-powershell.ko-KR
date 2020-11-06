---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: fb0565232410e840ef3e8adbad48e7f622a51d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532899"
---
# <span data-ttu-id="e32ed-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="e32ed-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="e32ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e32ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e32ed-103">계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e32ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e32ed-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="e32ed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e32ed-105">DESCRIPTION</span></span>
<span data-ttu-id="e32ed-106">**AzureStorageSASToken** Cmdlet은 Azure 저장소 계정에 대 한 sa (계정 수준 공유 액세스 서명) 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="e32ed-107">SAS 토큰을 사용 하 여 여러 서비스에 대 한 사용 권한을 위임 하거나 개체 수준 SAS 토큰과 함께 사용할 수 없는 서비스에 대 한 사용 권한을 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="e32ed-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e32ed-108">EXAMPLES</span></span>

### <span data-ttu-id="e32ed-109">예제 1: 모든 권한이 있는 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="e32ed-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="e32ed-110">이 명령은 모든 권한이 있는 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="e32ed-111">예제 2: IP 주소 범위에 대 한 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="e32ed-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="e32ed-112">이 명령은 지정 된 IP 주소 범위의 HTTPS 전용 요청에 대 한 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="e32ed-113">변수</span><span class="sxs-lookup"><span data-stu-id="e32ed-113">PARAMETERS</span></span>

### <span data-ttu-id="e32ed-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e32ed-114">-Context</span></span>
<span data-ttu-id="e32ed-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e32ed-116">New-AzureStorageContext cmdlet을 사용 하 여 **Azurestoragecontext** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="e32ed-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e32ed-117">-ExpiryTime</span></span>
<span data-ttu-id="e32ed-118">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="e32ed-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e32ed-119">-IPAddressOrRange</span></span>
<span data-ttu-id="e32ed-120">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e32ed-121">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="e32ed-122">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="e32ed-122">-Permission</span></span>
<span data-ttu-id="e32ed-123">저장소 계정에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="e32ed-124">사용 권한은 지정 된 리소스 종류와 일치 하는 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="e32ed-125">허용 되는 사용 권한 값에 대 한 자세한 내용은 계정 SA 만들기를 참조 하세요.https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="e32ed-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="e32ed-126">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="e32ed-126">-Protocol</span></span>
<span data-ttu-id="e32ed-127">계정 SA로 작성 된 요청에 허용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="e32ed-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e32ed-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e32ed-129">HttpsOnly</span></span>
- <span data-ttu-id="e32ed-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e32ed-130">HttpsOrHttp</span></span>

<span data-ttu-id="e32ed-131">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="e32ed-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e32ed-132">-ResourceType</span></span>
<span data-ttu-id="e32ed-133">SAS 토큰과 함께 사용할 수 있는 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="e32ed-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e32ed-135">않아야</span><span class="sxs-lookup"><span data-stu-id="e32ed-135">None</span></span>
- <span data-ttu-id="e32ed-136">Services</span><span class="sxs-lookup"><span data-stu-id="e32ed-136">Service</span></span>
- <span data-ttu-id="e32ed-137">컨트롤러</span><span class="sxs-lookup"><span data-stu-id="e32ed-137">Container</span></span>
- <span data-ttu-id="e32ed-138">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="e32ed-138">Object</span></span>

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

### <span data-ttu-id="e32ed-139">-서비스</span><span class="sxs-lookup"><span data-stu-id="e32ed-139">-Service</span></span>
<span data-ttu-id="e32ed-140">서비스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-140">Specifies the service.</span></span>
<span data-ttu-id="e32ed-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e32ed-142">않아야</span><span class="sxs-lookup"><span data-stu-id="e32ed-142">None</span></span>
- <span data-ttu-id="e32ed-143">블</span><span class="sxs-lookup"><span data-stu-id="e32ed-143">Blob</span></span>
- <span data-ttu-id="e32ed-144">파일</span><span class="sxs-lookup"><span data-stu-id="e32ed-144">File</span></span>
- <span data-ttu-id="e32ed-145">전담팀</span><span class="sxs-lookup"><span data-stu-id="e32ed-145">Queue</span></span>
- <span data-ttu-id="e32ed-146">테이블로</span><span class="sxs-lookup"><span data-stu-id="e32ed-146">Table</span></span>

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

### <span data-ttu-id="e32ed-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e32ed-147">-StartTime</span></span>
<span data-ttu-id="e32ed-148">SA가 유효 하 게 되는 **DateTime** 개체로 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="e32ed-149">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="e32ed-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32ed-150">CommonParameters</span></span>
<span data-ttu-id="e32ed-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32ed-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32ed-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32ed-153">입력</span><span class="sxs-lookup"><span data-stu-id="e32ed-153">INPUTS</span></span>

### <span data-ttu-id="e32ed-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e32ed-154">IStorageContext</span></span>

<span data-ttu-id="e32ed-155">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32ed-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e32ed-156">출력</span><span class="sxs-lookup"><span data-stu-id="e32ed-156">OUTPUTS</span></span>

### <span data-ttu-id="e32ed-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e32ed-157">System.String</span></span>

## <span data-ttu-id="e32ed-158">상속자</span><span class="sxs-lookup"><span data-stu-id="e32ed-158">NOTES</span></span>

## <span data-ttu-id="e32ed-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e32ed-159">RELATED LINKS</span></span>

[<span data-ttu-id="e32ed-160">새로운 AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e32ed-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="e32ed-161">새로운 AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e32ed-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="e32ed-162">새로운 AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="e32ed-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="e32ed-163">새로운 AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="e32ed-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="e32ed-164">새로운 AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="e32ed-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="e32ed-165">새로운 AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="e32ed-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


