---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178580"
---
# <span data-ttu-id="9a21d-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="9a21d-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="9a21d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a21d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a21d-103">주어진 NameSpace 이름 또는 별칭(DR 구성 이름)의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="9a21d-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="9a21d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a21d-104">SYNTAX</span></span>

### <span data-ttu-id="9a21d-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9a21d-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a21d-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9a21d-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a21d-107">설명</span><span class="sxs-lookup"><span data-stu-id="9a21d-107">DESCRIPTION</span></span>
<span data-ttu-id="9a21d-108">**Test-AzServiceBusName** Cmdlet NameSpace 이름 또는 별칭의 가용성 확인(DR 구성 이름)</span><span class="sxs-lookup"><span data-stu-id="9a21d-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="9a21d-109">예제</span><span class="sxs-lookup"><span data-stu-id="9a21d-109">EXAMPLES</span></span>

### <span data-ttu-id="9a21d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a21d-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="9a21d-111">네임스페이스 이름 'MyNameSapceName'의 가용성 상태를 True로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9a21d-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="9a21d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9a21d-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="9a21d-113">'MyNameSapceName' 네임스페이스 이름의 가용성에 대한 상태를 이유로 False로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9a21d-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="9a21d-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="9a21d-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="9a21d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a21d-115">PARAMETERS</span></span>

### <span data-ttu-id="9a21d-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="9a21d-116">-AliasName</span></span>
<span data-ttu-id="9a21d-117">DR 구성 이름 - 별칭 이름</span><span class="sxs-lookup"><span data-stu-id="9a21d-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a21d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a21d-118">-DefaultProfile</span></span>
<span data-ttu-id="9a21d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a21d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a21d-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a21d-120">-Namespace</span></span>
<span data-ttu-id="9a21d-121">Servicebus 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="9a21d-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a21d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a21d-122">-ResourceGroupName</span></span>
<span data-ttu-id="9a21d-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9a21d-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a21d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a21d-124">CommonParameters</span></span>
<span data-ttu-id="9a21d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a21d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a21d-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9a21d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a21d-127">입력</span><span class="sxs-lookup"><span data-stu-id="9a21d-127">INPUTS</span></span>

### <span data-ttu-id="9a21d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9a21d-128">System.String</span></span>

## <span data-ttu-id="9a21d-129">출력</span><span class="sxs-lookup"><span data-stu-id="9a21d-129">OUTPUTS</span></span>

### <span data-ttu-id="9a21d-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="9a21d-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="9a21d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a21d-131">NOTES</span></span>

## <span data-ttu-id="9a21d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a21d-132">RELATED LINKS</span></span>
