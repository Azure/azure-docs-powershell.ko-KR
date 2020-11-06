---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac818fd403df9b159671f5889e068bda82a086d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523664"
---
# <span data-ttu-id="b1a1a-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="b1a1a-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="b1a1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a1a-103">Azure 저장소 큐에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="b1a1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1a1a-104">SYNTAX</span></span>

### <span data-ttu-id="b1a1a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="b1a1a-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="b1a1a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="b1a1a-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="b1a1a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b1a1a-107">DESCRIPTION</span></span>
<span data-ttu-id="b1a1a-108">**AzureStorageQueueSASToken** Cmdlet은 Azure 저장소 큐에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="b1a1a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b1a1a-109">EXAMPLES</span></span>

### <span data-ttu-id="b1a1a-110">예제 1: 모든 권한이 있는 큐 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="b1a1a-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="b1a1a-111">이 예제에서는 모든 권한이 있는 큐 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="b1a1a-112">변수</span><span class="sxs-lookup"><span data-stu-id="b1a1a-112">PARAMETERS</span></span>

### <span data-ttu-id="b1a1a-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b1a1a-113">-Context</span></span>
<span data-ttu-id="b1a1a-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b1a1a-115">New-AzureStorageContext cmdlet을 통해 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b1a1a-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b1a1a-116">-ExpiryTime</span></span>
<span data-ttu-id="b1a1a-117">공유 액세스 서명이 더 이상 유효 하지 않은 경우를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="b1a1a-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b1a1a-118">-FullUri</span></span>
<span data-ttu-id="b1a1a-119">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="b1a1a-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b1a1a-120">-IPAddressOrRange</span></span>
<span data-ttu-id="b1a1a-121">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b1a1a-122">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="b1a1a-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b1a1a-123">-Name</span></span>
<span data-ttu-id="b1a1a-124">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a1a-125">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="b1a1a-125">-Permission</span></span>
<span data-ttu-id="b1a1a-126">저장소 큐에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="b1a1a-127">-정책</span><span class="sxs-lookup"><span data-stu-id="b1a1a-127">-Policy</span></span>
<span data-ttu-id="b1a1a-128">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="b1a1a-129">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="b1a1a-129">-Protocol</span></span>
<span data-ttu-id="b1a1a-130">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b1a1a-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b1a1a-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b1a1a-132">HttpsOnly</span></span>
* <span data-ttu-id="b1a1a-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="b1a1a-133">HttpsOrHttp</span></span>

<span data-ttu-id="b1a1a-134">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b1a1a-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b1a1a-135">-StartTime</span></span>
<span data-ttu-id="b1a1a-136">공유 액세스 서명이 유효한 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="b1a1a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a1a-137">CommonParameters</span></span>
<span data-ttu-id="b1a1a-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a1a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a1a-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a1a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a1a-140">입력</span><span class="sxs-lookup"><span data-stu-id="b1a1a-140">INPUTS</span></span>

## <span data-ttu-id="b1a1a-141">출력</span><span class="sxs-lookup"><span data-stu-id="b1a1a-141">OUTPUTS</span></span>

## <span data-ttu-id="b1a1a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="b1a1a-142">NOTES</span></span>

## <span data-ttu-id="b1a1a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1a1a-143">RELATED LINKS</span></span>

