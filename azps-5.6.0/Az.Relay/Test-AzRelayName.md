---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: be0b0f2aa9aa45fa69b3d57051a5671a76186abc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000336"
---
# <span data-ttu-id="21217-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="21217-101">Test-AzRelayName</span></span>

## <span data-ttu-id="21217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21217-102">SYNOPSIS</span></span>
<span data-ttu-id="21217-103">지정한 NameSpace 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="21217-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="21217-104">구문</span><span class="sxs-lookup"><span data-stu-id="21217-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21217-105">설명</span><span class="sxs-lookup"><span data-stu-id="21217-105">DESCRIPTION</span></span>
<span data-ttu-id="21217-106">**NameSpace 이름의 Test-AzRelayName** Cmdlet 확인</span><span class="sxs-lookup"><span data-stu-id="21217-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="21217-107">예제</span><span class="sxs-lookup"><span data-stu-id="21217-107">EXAMPLES</span></span>

### <span data-ttu-id="21217-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="21217-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="21217-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="21217-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="21217-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="21217-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="21217-111">네임스페이스 이름의 가용성에 대한 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="21217-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="21217-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21217-112">PARAMETERS</span></span>

### <span data-ttu-id="21217-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21217-113">-DefaultProfile</span></span>
<span data-ttu-id="21217-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21217-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21217-115">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="21217-115">-Namespace</span></span>
<span data-ttu-id="21217-116">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21217-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="21217-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21217-117">CommonParameters</span></span>
<span data-ttu-id="21217-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21217-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21217-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21217-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21217-120">입력</span><span class="sxs-lookup"><span data-stu-id="21217-120">INPUTS</span></span>

### <span data-ttu-id="21217-121">System.String</span><span class="sxs-lookup"><span data-stu-id="21217-121">System.String</span></span>

## <span data-ttu-id="21217-122">출력</span><span class="sxs-lookup"><span data-stu-id="21217-122">OUTPUTS</span></span>

### <span data-ttu-id="21217-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="21217-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="21217-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21217-124">NOTES</span></span>

## <span data-ttu-id="21217-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21217-125">RELATED LINKS</span></span>
