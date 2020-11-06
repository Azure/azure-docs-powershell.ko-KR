---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
ms.openlocfilehash: 0e8ad44ebbd8a5585626de27317caa14b408f87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532895"
---
# <span data-ttu-id="5f5a3-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5f5a3-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="5f5a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5a3-103">Azure 저장소 컨테이너에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f5a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f5a3-104">SYNTAX</span></span>

### <span data-ttu-id="5f5a3-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="5f5a3-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="5f5a3-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="5f5a3-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5f5a3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5f5a3-107">DESCRIPTION</span></span>
<span data-ttu-id="5f5a3-108">**AzureStorageContainerSASToken** Cmdlet은 Azure 저장소 컨테이너에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="5f5a3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5f5a3-109">EXAMPLES</span></span>

### <span data-ttu-id="5f5a3-110">예제 1: 전체 컨테이너 권한을 사용 하 여 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="5f5a3-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="5f5a3-111">이 예제에서는 모든 컨테이너 권한이 있는 컨테이너 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="5f5a3-112">예제 2: 파이프라인을 통해 다중 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="5f5a3-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="5f5a3-113">이 예제에서는 파이프라인을 사용 하 여 컨테이너 SAS 토큰을 여러 개 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="5f5a3-114">예제 3: 공유 액세스 정책을 사용 하 여 컨테이너 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="5f5a3-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="5f5a3-115">이 예제에서는 공유 액세스 정책을 사용 하 여 컨테이너 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="5f5a3-116">변수</span><span class="sxs-lookup"><span data-stu-id="5f5a3-116">PARAMETERS</span></span>

### <span data-ttu-id="5f5a3-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5f5a3-117">-Context</span></span>
<span data-ttu-id="5f5a3-118">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5f5a3-119">New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5f5a3-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5f5a3-120">-ExpiryTime</span></span>
<span data-ttu-id="5f5a3-121">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="5f5a3-122">사용자가 시작 시간을 설정 했지만 만료 시간이 아닌 경우 만료 시간은 시작 시간에 1 시간을 더한 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="5f5a3-123">시작 시간이 나 만료 시간이 모두 지정 되어 있지 않은 경우 만료 시간은 현재 시간에 1 시간을 더한 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="5f5a3-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5f5a3-124">-FullUri</span></span>
<span data-ttu-id="5f5a3-125">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="5f5a3-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5f5a3-126">-IPAddressOrRange</span></span>
<span data-ttu-id="5f5a3-127">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5f5a3-128">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="5f5a3-129">-이름</span><span class="sxs-lookup"><span data-stu-id="5f5a3-129">-Name</span></span>
<span data-ttu-id="5f5a3-130">Azure 저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f5a3-131">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="5f5a3-131">-Permission</span></span>
<span data-ttu-id="5f5a3-132">저장소 컨테이너에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="5f5a3-133">-정책</span><span class="sxs-lookup"><span data-stu-id="5f5a3-133">-Policy</span></span>
<span data-ttu-id="5f5a3-134">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="5f5a3-135">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="5f5a3-135">-Protocol</span></span>
<span data-ttu-id="5f5a3-136">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5f5a3-137">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5f5a3-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5f5a3-138">HttpsOnly</span></span>
* <span data-ttu-id="5f5a3-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="5f5a3-139">HttpsOrHttp</span></span>

<span data-ttu-id="5f5a3-140">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5f5a3-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5f5a3-141">-StartTime</span></span>
<span data-ttu-id="5f5a3-142">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="5f5a3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5a3-143">CommonParameters</span></span>
<span data-ttu-id="5f5a3-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5a3-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5a3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5a3-146">입력</span><span class="sxs-lookup"><span data-stu-id="5f5a3-146">INPUTS</span></span>

### <span data-ttu-id="5f5a3-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f5a3-147">IStorageContext</span></span>

<span data-ttu-id="5f5a3-148">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5f5a3-149">이름</span><span class="sxs-lookup"><span data-stu-id="5f5a3-149">String</span></span>

<span data-ttu-id="5f5a3-150">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5a3-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5f5a3-151">출력</span><span class="sxs-lookup"><span data-stu-id="5f5a3-151">OUTPUTS</span></span>

### <span data-ttu-id="5f5a3-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f5a3-152">System.String</span></span>

## <span data-ttu-id="5f5a3-153">상속자</span><span class="sxs-lookup"><span data-stu-id="5f5a3-153">NOTES</span></span>

## <span data-ttu-id="5f5a3-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f5a3-154">RELATED LINKS</span></span>

[<span data-ttu-id="5f5a3-155">새로운 AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5f5a3-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
