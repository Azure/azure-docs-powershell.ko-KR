---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533316"
---
# <span data-ttu-id="2356c-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="2356c-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="2356c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2356c-102">SYNOPSIS</span></span>
<span data-ttu-id="2356c-103">지정 된 네임 스페이스 이름 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356c-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2356c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2356c-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2356c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2356c-105">DESCRIPTION</span></span>
<span data-ttu-id="2356c-106">네임 스페이스 이름의 **AzureRmRelayName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="2356c-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="2356c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2356c-107">EXAMPLES</span></span>

### <span data-ttu-id="2356c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2356c-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="2356c-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="2356c-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="2356c-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="2356c-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="2356c-111">네임 스페이스 이름 사용 가능성에 대 한 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356c-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="2356c-112">변수</span><span class="sxs-lookup"><span data-stu-id="2356c-112">PARAMETERS</span></span>

### <span data-ttu-id="2356c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2356c-113">-DefaultProfile</span></span>
<span data-ttu-id="2356c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2356c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2356c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2356c-115">-Namespace</span></span>
<span data-ttu-id="2356c-116">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2356c-116">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2356c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2356c-117">CommonParameters</span></span>
<span data-ttu-id="2356c-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2356c-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2356c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2356c-120">입력</span><span class="sxs-lookup"><span data-stu-id="2356c-120">INPUTS</span></span>

### <span data-ttu-id="2356c-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2356c-121">System.String</span></span>


## <span data-ttu-id="2356c-122">출력</span><span class="sxs-lookup"><span data-stu-id="2356c-122">OUTPUTS</span></span>

### <span data-ttu-id="2356c-123">PSCheckNameAvailabilityResultAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="2356c-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="2356c-124">상속자</span><span class="sxs-lookup"><span data-stu-id="2356c-124">NOTES</span></span>

## <span data-ttu-id="2356c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2356c-125">RELATED LINKS</span></span>
