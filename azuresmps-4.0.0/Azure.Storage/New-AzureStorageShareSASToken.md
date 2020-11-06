---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523564"
---
# <span data-ttu-id="d4103-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="d4103-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="d4103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4103-102">SYNOPSIS</span></span>
<span data-ttu-id="d4103-103">Azure 저장소 공유에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="d4103-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4103-104">SYNTAX</span></span>

### <span data-ttu-id="d4103-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="d4103-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d4103-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="d4103-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d4103-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d4103-107">DESCRIPTION</span></span>
<span data-ttu-id="d4103-108">**AzureStorageShareSASToken** Cmdlet은 Azure 저장소 공유에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="d4103-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d4103-109">EXAMPLES</span></span>

### <span data-ttu-id="d4103-110">예제 1: 공유에 대 한 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="d4103-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="d4103-111">이 명령은 ContosoShare 이라는 공유에 대 한 공유 액세스 서명 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="d4103-112">예제 2: 파이프라인을 사용 하 여 여러 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="d4103-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="d4103-113">이 명령은 접두사 테스트와 일치 하는 모든 저장소 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="d4103-114">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d4103-115">현재 cmdlet은 지정 된 사용 권한을 가진 각 저장소 공유에 대 한 공유 액세스 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="d4103-116">예제 3: 공유 액세스 정책을 사용 하는 공유 액세스 서명 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="d4103-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="d4103-117">이 명령은 ContosoPolicy03 이라는 정책이 있는 ContosoShare 이라는 저장소 공유에 대 한 공유 액세스 서명 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="d4103-118">변수</span><span class="sxs-lookup"><span data-stu-id="d4103-118">PARAMETERS</span></span>

### <span data-ttu-id="d4103-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d4103-119">-Context</span></span>
<span data-ttu-id="d4103-120">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d4103-121">컨텍스트를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d4103-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d4103-122">-ExpiryTime</span></span>
<span data-ttu-id="d4103-123">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="d4103-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d4103-124">-FullUri</span></span>
<span data-ttu-id="d4103-125">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d4103-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d4103-126">-IPAddressOrRange</span></span>
<span data-ttu-id="d4103-127">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d4103-128">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="d4103-129">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="d4103-129">-Permission</span></span>
<span data-ttu-id="d4103-130">공유 아래에 있는 공유 및 파일에 액세스할 수 있는 토큰의 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

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

### <span data-ttu-id="d4103-131">-정책</span><span class="sxs-lookup"><span data-stu-id="d4103-131">-Policy</span></span>
<span data-ttu-id="d4103-132">공유에 대 한 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-132">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="d4103-133">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="d4103-133">-Protocol</span></span>
<span data-ttu-id="d4103-134">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d4103-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d4103-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d4103-136">HttpsOnly</span></span>
* <span data-ttu-id="d4103-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="d4103-137">HttpsOrHttp</span></span>

<span data-ttu-id="d4103-138">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="d4103-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d4103-139">-ShareName</span></span>
<span data-ttu-id="d4103-140">저장소 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4103-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d4103-141">-StartTime</span></span>
<span data-ttu-id="d4103-142">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d4103-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4103-143">CommonParameters</span></span>
<span data-ttu-id="d4103-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4103-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4103-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4103-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4103-146">입력</span><span class="sxs-lookup"><span data-stu-id="d4103-146">INPUTS</span></span>

## <span data-ttu-id="d4103-147">출력</span><span class="sxs-lookup"><span data-stu-id="d4103-147">OUTPUTS</span></span>

## <span data-ttu-id="d4103-148">상속자</span><span class="sxs-lookup"><span data-stu-id="d4103-148">NOTES</span></span>
* <span data-ttu-id="d4103-149">키워드: common, azure, services, data, 저장소, blob, 대기열, 테이블</span><span class="sxs-lookup"><span data-stu-id="d4103-149">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="d4103-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4103-150">RELATED LINKS</span></span>

[<span data-ttu-id="d4103-151">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4103-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="d4103-152">새로운 AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="d4103-152">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
