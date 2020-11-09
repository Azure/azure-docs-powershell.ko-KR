---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308000"
---
# <span data-ttu-id="b8d53-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="b8d53-101">Test-AzRelayName</span></span>

## <span data-ttu-id="b8d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8d53-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d53-103">지정 된 네임 스페이스 이름 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d53-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="b8d53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8d53-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d53-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8d53-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d53-106">네임 스페이스 이름의 **AzRelayName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="b8d53-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="b8d53-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8d53-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d53-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8d53-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="b8d53-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="b8d53-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="b8d53-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="b8d53-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="b8d53-111">네임 스페이스 이름 사용 가능성에 대 한 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d53-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="b8d53-112">변수</span><span class="sxs-lookup"><span data-stu-id="b8d53-112">PARAMETERS</span></span>

### <span data-ttu-id="b8d53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d53-113">-DefaultProfile</span></span>
<span data-ttu-id="b8d53-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d53-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8d53-115">-Namespace</span></span>
<span data-ttu-id="b8d53-116">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d53-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="b8d53-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d53-117">CommonParameters</span></span>
<span data-ttu-id="b8d53-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d53-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d53-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d53-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d53-120">입력</span><span class="sxs-lookup"><span data-stu-id="b8d53-120">INPUTS</span></span>

### <span data-ttu-id="b8d53-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8d53-121">System.String</span></span>

## <span data-ttu-id="b8d53-122">출력</span><span class="sxs-lookup"><span data-stu-id="b8d53-122">OUTPUTS</span></span>

### <span data-ttu-id="b8d53-123">PSCheckNameAvailabilityResultAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="b8d53-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="b8d53-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b8d53-124">NOTES</span></span>

## <span data-ttu-id="b8d53-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8d53-125">RELATED LINKS</span></span>
