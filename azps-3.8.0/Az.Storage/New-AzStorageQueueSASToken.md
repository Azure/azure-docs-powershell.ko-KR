---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043473"
---
# <span data-ttu-id="0323b-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="0323b-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="0323b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0323b-102">SYNOPSIS</span></span>
<span data-ttu-id="0323b-103">Azure 저장소 큐에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="0323b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0323b-104">SYNTAX</span></span>

### <span data-ttu-id="0323b-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="0323b-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0323b-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="0323b-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0323b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0323b-107">DESCRIPTION</span></span>
<span data-ttu-id="0323b-108">**AzStorageQueueSASToken** Cmdlet은 Azure 저장소 큐에 대 한 공유 액세스 서명 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="0323b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0323b-109">EXAMPLES</span></span>

### <span data-ttu-id="0323b-110">예제 1: 모든 권한이 있는 큐 SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="0323b-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="0323b-111">이 예제에서는 모든 권한이 있는 큐 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="0323b-112">변수</span><span class="sxs-lookup"><span data-stu-id="0323b-112">PARAMETERS</span></span>

### <span data-ttu-id="0323b-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0323b-113">-Context</span></span>
<span data-ttu-id="0323b-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0323b-115">New-AzStorageContext cmdlet을 통해 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0323b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0323b-116">-DefaultProfile</span></span>
<span data-ttu-id="0323b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0323b-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0323b-118">-ExpiryTime</span></span>
<span data-ttu-id="0323b-119">공유 액세스 서명이 더 이상 유효 하지 않은 경우를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="0323b-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="0323b-120">-FullUri</span></span>
<span data-ttu-id="0323b-121">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="0323b-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0323b-122">-IPAddressOrRange</span></span>
<span data-ttu-id="0323b-123">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="0323b-124">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="0323b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="0323b-125">-Name</span></span>
<span data-ttu-id="0323b-126">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0323b-127">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="0323b-127">-Permission</span></span>
<span data-ttu-id="0323b-128">저장소 큐에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="0323b-129">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="0323b-130">-정책</span><span class="sxs-lookup"><span data-stu-id="0323b-130">-Policy</span></span>
<span data-ttu-id="0323b-131">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="0323b-132">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="0323b-132">-Protocol</span></span>
<span data-ttu-id="0323b-133">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="0323b-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="0323b-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0323b-135">HttpsOnly</span></span>
* <span data-ttu-id="0323b-136">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0323b-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0323b-137">-StartTime</span></span>
<span data-ttu-id="0323b-138">공유 액세스 서명이 유효한 시기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="0323b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0323b-139">CommonParameters</span></span>
<span data-ttu-id="0323b-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0323b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0323b-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0323b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0323b-142">입력</span><span class="sxs-lookup"><span data-stu-id="0323b-142">INPUTS</span></span>

### <span data-ttu-id="0323b-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0323b-143">System.String</span></span>

### <span data-ttu-id="0323b-144">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0323b-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0323b-145">출력</span><span class="sxs-lookup"><span data-stu-id="0323b-145">OUTPUTS</span></span>

### <span data-ttu-id="0323b-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0323b-146">System.String</span></span>

## <span data-ttu-id="0323b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0323b-147">NOTES</span></span>

## <span data-ttu-id="0323b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0323b-148">RELATED LINKS</span></span>