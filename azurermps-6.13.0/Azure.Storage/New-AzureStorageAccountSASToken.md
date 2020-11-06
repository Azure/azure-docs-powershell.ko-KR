---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: 8b0eb67808bf4148d93006b24273d55b737adfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531563"
---
# <span data-ttu-id="4e0f8-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="4e0f8-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="4e0f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0f8-103">계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e0f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e0f8-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e0f8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4e0f8-105">DESCRIPTION</span></span>
<span data-ttu-id="4e0f8-106">**AzureStorageSASToken** Cmdlet은 Azure 저장소 계정에 대 한 sa (계정 수준 공유 액세스 서명) 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="4e0f8-107">SAS 토큰을 사용 하 여 여러 서비스에 대 한 사용 권한을 위임 하거나 개체 수준 SAS 토큰과 함께 사용할 수 없는 서비스에 대 한 사용 권한을 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="4e0f8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4e0f8-108">EXAMPLES</span></span>

### <span data-ttu-id="4e0f8-109">예제 1: 모든 권한이 있는 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="4e0f8-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="4e0f8-110">이 명령은 모든 권한이 있는 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="4e0f8-111">예제 2: IP 주소 범위에 대 한 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="4e0f8-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="4e0f8-112">이 명령은 지정 된 IP 주소 범위의 HTTPS 전용 요청에 대 한 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="4e0f8-113">변수</span><span class="sxs-lookup"><span data-stu-id="4e0f8-113">PARAMETERS</span></span>

### <span data-ttu-id="4e0f8-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4e0f8-114">-Context</span></span>
<span data-ttu-id="4e0f8-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4e0f8-116">New-AzureStorageContext cmdlet을 사용 하 여 **Azurestoragecontext** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="4e0f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0f8-117">-DefaultProfile</span></span>
<span data-ttu-id="4e0f8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0f8-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4e0f8-119">-ExpiryTime</span></span>
<span data-ttu-id="4e0f8-120">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="4e0f8-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4e0f8-121">-IPAddressOrRange</span></span>
<span data-ttu-id="4e0f8-122">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4e0f8-123">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="4e0f8-124">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="4e0f8-124">-Permission</span></span>
<span data-ttu-id="4e0f8-125">저장소 계정에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="4e0f8-126">사용 권한은 지정 된 리소스 종류와 일치 하는 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="4e0f8-127">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="4e0f8-128">허용 되는 사용 권한 값에 대 한 자세한 내용은 계정 SA 만들기를 참조 하세요. https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="4e0f8-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="4e0f8-129">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="4e0f8-129">-Protocol</span></span>
<span data-ttu-id="4e0f8-130">계정 SA로 작성 된 요청에 허용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="4e0f8-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e0f8-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4e0f8-132">HttpsOnly</span></span>
- <span data-ttu-id="4e0f8-133">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0f8-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4e0f8-134">-ResourceType</span></span>
<span data-ttu-id="4e0f8-135">SAS 토큰과 함께 사용할 수 있는 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="4e0f8-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e0f8-137">않아야</span><span class="sxs-lookup"><span data-stu-id="4e0f8-137">None</span></span>
- <span data-ttu-id="4e0f8-138">Services</span><span class="sxs-lookup"><span data-stu-id="4e0f8-138">Service</span></span>
- <span data-ttu-id="4e0f8-139">컨트롤러</span><span class="sxs-lookup"><span data-stu-id="4e0f8-139">Container</span></span>
- <span data-ttu-id="4e0f8-140">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="4e0f8-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0f8-141">-서비스</span><span class="sxs-lookup"><span data-stu-id="4e0f8-141">-Service</span></span>
<span data-ttu-id="4e0f8-142">서비스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-142">Specifies the service.</span></span>
<span data-ttu-id="4e0f8-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e0f8-144">않아야</span><span class="sxs-lookup"><span data-stu-id="4e0f8-144">None</span></span>
- <span data-ttu-id="4e0f8-145">블</span><span class="sxs-lookup"><span data-stu-id="4e0f8-145">Blob</span></span>
- <span data-ttu-id="4e0f8-146">파일</span><span class="sxs-lookup"><span data-stu-id="4e0f8-146">File</span></span>
- <span data-ttu-id="4e0f8-147">전담팀</span><span class="sxs-lookup"><span data-stu-id="4e0f8-147">Queue</span></span>
- <span data-ttu-id="4e0f8-148">테이블로</span><span class="sxs-lookup"><span data-stu-id="4e0f8-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0f8-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4e0f8-149">-StartTime</span></span>
<span data-ttu-id="4e0f8-150">SA가 유효 하 게 되는 **DateTime** 개체로 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="4e0f8-151">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4e0f8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0f8-152">CommonParameters</span></span>
<span data-ttu-id="4e0f8-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0f8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0f8-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0f8-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0f8-155">입력</span><span class="sxs-lookup"><span data-stu-id="4e0f8-155">INPUTS</span></span>

### <span data-ttu-id="4e0f8-156">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e0f8-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e0f8-157">출력</span><span class="sxs-lookup"><span data-stu-id="4e0f8-157">OUTPUTS</span></span>

### <span data-ttu-id="4e0f8-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4e0f8-158">System.String</span></span>

## <span data-ttu-id="4e0f8-159">상속자</span><span class="sxs-lookup"><span data-stu-id="4e0f8-159">NOTES</span></span>

## <span data-ttu-id="4e0f8-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e0f8-160">RELATED LINKS</span></span>

[<span data-ttu-id="4e0f8-161">새로운 AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4e0f8-161">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="4e0f8-162">새로운 AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4e0f8-162">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="4e0f8-163">새로운 AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="4e0f8-163">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="4e0f8-164">새로운 AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="4e0f8-164">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="4e0f8-165">새로운 AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="4e0f8-165">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="4e0f8-166">새로운 AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="4e0f8-166">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


