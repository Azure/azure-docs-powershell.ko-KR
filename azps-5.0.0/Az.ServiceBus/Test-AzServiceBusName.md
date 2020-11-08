---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226330"
---
# <span data-ttu-id="e125c-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="e125c-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="e125c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e125c-102">SYNOPSIS</span></span>
<span data-ttu-id="e125c-103">지정 된 네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e125c-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="e125c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e125c-104">SYNTAX</span></span>

### <span data-ttu-id="e125c-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e125c-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e125c-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e125c-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e125c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e125c-107">DESCRIPTION</span></span>
<span data-ttu-id="e125c-108">네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 **AzServiceBusName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="e125c-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="e125c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e125c-109">EXAMPLES</span></span>

### <span data-ttu-id="e125c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e125c-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="e125c-111">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e125c-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="e125c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e125c-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="e125c-113">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 False로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e125c-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="e125c-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="e125c-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="e125c-115">변수</span><span class="sxs-lookup"><span data-stu-id="e125c-115">PARAMETERS</span></span>

### <span data-ttu-id="e125c-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e125c-116">-AliasName</span></span>
<span data-ttu-id="e125c-117">DR 구성 이름-별칭 이름</span><span class="sxs-lookup"><span data-stu-id="e125c-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="e125c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e125c-118">-DefaultProfile</span></span>
<span data-ttu-id="e125c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e125c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e125c-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e125c-120">-Namespace</span></span>
<span data-ttu-id="e125c-121">Servicebus 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e125c-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="e125c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e125c-122">-ResourceGroupName</span></span>
<span data-ttu-id="e125c-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e125c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e125c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e125c-124">CommonParameters</span></span>
<span data-ttu-id="e125c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e125c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e125c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e125c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e125c-127">입력</span><span class="sxs-lookup"><span data-stu-id="e125c-127">INPUTS</span></span>

### <span data-ttu-id="e125c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e125c-128">System.String</span></span>

## <span data-ttu-id="e125c-129">출력</span><span class="sxs-lookup"><span data-stu-id="e125c-129">OUTPUTS</span></span>

### <span data-ttu-id="e125c-130">ServiceBus. PSCheckNameAvailabilityResultAttributes/.</span><span class="sxs-lookup"><span data-stu-id="e125c-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="e125c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e125c-131">NOTES</span></span>

## <span data-ttu-id="e125c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e125c-132">RELATED LINKS</span></span>
