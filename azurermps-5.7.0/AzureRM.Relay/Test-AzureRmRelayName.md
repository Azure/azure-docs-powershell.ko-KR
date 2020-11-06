---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531675"
---
# <span data-ttu-id="bb0c4-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="bb0c4-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="bb0c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0c4-103">지정 된 네임 스페이스 이름 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb0c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb0c4-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb0c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="bb0c4-106">네임 스페이스 이름의 **AzureRmRelayName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="bb0c4-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="bb0c4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb0c4-107">EXAMPLES</span></span>

### <span data-ttu-id="bb0c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb0c4-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="bb0c4-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="bb0c4-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="bb0c4-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="bb0c4-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="bb0c4-111">네임 스페이스 이름 사용 가능성에 대 한 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="bb0c4-112">변수</span><span class="sxs-lookup"><span data-stu-id="bb0c4-112">PARAMETERS</span></span>

### <span data-ttu-id="bb0c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0c4-113">-DefaultProfile</span></span>
<span data-ttu-id="bb0c4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0c4-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb0c4-115">-Namespace</span></span>
<span data-ttu-id="bb0c4-116">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="bb0c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0c4-117">CommonParameters</span></span>
<span data-ttu-id="bb0c4-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0c4-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb0c4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0c4-120">입력</span><span class="sxs-lookup"><span data-stu-id="bb0c4-120">INPUTS</span></span>

### <span data-ttu-id="bb0c4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb0c4-121">-Namespace</span></span>
 <span data-ttu-id="bb0c4-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb0c4-122">System.String</span></span>

## <span data-ttu-id="bb0c4-123">출력</span><span class="sxs-lookup"><span data-stu-id="bb0c4-123">OUTPUTS</span></span>

### <span data-ttu-id="bb0c4-124">[CheckNameAvailabilityResultAttributes, Microsoft Azure. 0.1.0.0, Version =, Culture = 중립, PublicKeyToken = null] 등의 명령을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="bb0c4-125">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb0c4-125">Example 1</span></span>
<span data-ttu-id="bb0c4-126">이름 사용 가능한 이유 메시지</span><span class="sxs-lookup"><span data-stu-id="bb0c4-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="bb0c4-127">예제 2</span><span class="sxs-lookup"><span data-stu-id="bb0c4-127">Example 2</span></span>
<span data-ttu-id="bb0c4-128">이름 사용 가능한 이유 메시지</span><span class="sxs-lookup"><span data-stu-id="bb0c4-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="bb0c4-129">예제 3</span><span class="sxs-lookup"><span data-stu-id="bb0c4-129">Example 3</span></span>
<span data-ttu-id="bb0c4-130">이름 사용 가능한 이유 메시지</span><span class="sxs-lookup"><span data-stu-id="bb0c4-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="bb0c4-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bb0c4-131">NOTES</span></span>

## <span data-ttu-id="bb0c4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb0c4-132">RELATED LINKS</span></span>

