---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208573"
---
# <span data-ttu-id="55924-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="55924-101">Test-AzRelayName</span></span>

## <span data-ttu-id="55924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55924-102">SYNOPSIS</span></span>
<span data-ttu-id="55924-103">주어진 NameSpace 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="55924-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="55924-104">구문</span><span class="sxs-lookup"><span data-stu-id="55924-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55924-105">설명</span><span class="sxs-lookup"><span data-stu-id="55924-105">DESCRIPTION</span></span>
<span data-ttu-id="55924-106">**Test-AzRelayName** Cmdlet NameSpace 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="55924-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="55924-107">예제</span><span class="sxs-lookup"><span data-stu-id="55924-107">EXAMPLES</span></span>

### <span data-ttu-id="55924-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="55924-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="55924-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="55924-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="55924-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="55924-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="55924-111">네임스페이스 이름의 가용성 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="55924-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="55924-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55924-112">PARAMETERS</span></span>

### <span data-ttu-id="55924-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55924-113">-DefaultProfile</span></span>
<span data-ttu-id="55924-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55924-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55924-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="55924-115">-Namespace</span></span>
<span data-ttu-id="55924-116">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55924-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="55924-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55924-117">CommonParameters</span></span>
<span data-ttu-id="55924-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55924-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55924-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="55924-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55924-120">입력</span><span class="sxs-lookup"><span data-stu-id="55924-120">INPUTS</span></span>

### <span data-ttu-id="55924-121">System.String</span><span class="sxs-lookup"><span data-stu-id="55924-121">System.String</span></span>

## <span data-ttu-id="55924-122">출력</span><span class="sxs-lookup"><span data-stu-id="55924-122">OUTPUTS</span></span>

### <span data-ttu-id="55924-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="55924-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="55924-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55924-124">NOTES</span></span>

## <span data-ttu-id="55924-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55924-125">RELATED LINKS</span></span>
