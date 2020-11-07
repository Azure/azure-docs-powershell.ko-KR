---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710943"
---
# <span data-ttu-id="4becc-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="4becc-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="4becc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4becc-102">SYNOPSIS</span></span>
<span data-ttu-id="4becc-103">지정 된 네임 스페이스 이름 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4becc-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4becc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4becc-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="4becc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4becc-105">DESCRIPTION</span></span>
<span data-ttu-id="4becc-106">네임 스페이스 이름의 **AzureRmServiceBusName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="4becc-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="4becc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4becc-107">EXAMPLES</span></span>

### <span data-ttu-id="4becc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4becc-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="4becc-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="4becc-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="4becc-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="4becc-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="4becc-111">네임 스페이스 이름 사용 가능성에 대 한 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4becc-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="4becc-112">변수</span><span class="sxs-lookup"><span data-stu-id="4becc-112">PARAMETERS</span></span>

### <span data-ttu-id="4becc-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4becc-113">-Namespace</span></span>
<span data-ttu-id="4becc-114">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4becc-114">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="4becc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4becc-115">CommonParameters</span></span>
<span data-ttu-id="4becc-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4becc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4becc-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4becc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4becc-118">입력</span><span class="sxs-lookup"><span data-stu-id="4becc-118">INPUTS</span></span>

### <span data-ttu-id="4becc-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4becc-119">-Namespace</span></span>
 <span data-ttu-id="4becc-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4becc-120">System.String</span></span>

## <span data-ttu-id="4becc-121">출력</span><span class="sxs-lookup"><span data-stu-id="4becc-121">OUTPUTS</span></span>

### <span data-ttu-id="4becc-122">[ServiceBus, CheckNameAvailabilityResultAttributes, ServiceBus, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null] 등의 명령을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4becc-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="4becc-123">예제 1</span><span class="sxs-lookup"><span data-stu-id="4becc-123">Example 1</span></span>
<span data-ttu-id="4becc-124">이름 사용 가능한 이유 메시지</span><span class="sxs-lookup"><span data-stu-id="4becc-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="4becc-125">예제 2</span><span class="sxs-lookup"><span data-stu-id="4becc-125">Example 2</span></span>
<span data-ttu-id="4becc-126">이름 사용 가능한 이유 메시지</span><span class="sxs-lookup"><span data-stu-id="4becc-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="4becc-127">예제 3</span><span class="sxs-lookup"><span data-stu-id="4becc-127">Example 3</span></span>
<span data-ttu-id="4becc-128">이름 사용 가능한 이유 메시지</span><span class="sxs-lookup"><span data-stu-id="4becc-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="4becc-129">상속자</span><span class="sxs-lookup"><span data-stu-id="4becc-129">NOTES</span></span>

## <span data-ttu-id="4becc-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4becc-130">RELATED LINKS</span></span>
