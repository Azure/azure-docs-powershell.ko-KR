---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8717019982175b30e0db84e7433147008e40803e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689904"
---
# <span data-ttu-id="42282-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="42282-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="42282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42282-102">SYNOPSIS</span></span>
<span data-ttu-id="42282-103">지정 된 네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="42282-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="42282-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42282-104">SYNTAX</span></span>

### <span data-ttu-id="42282-105">NamespaceCheckNameAvailabilitySet (기본값)</span><span class="sxs-lookup"><span data-stu-id="42282-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42282-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42282-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42282-107">설명은</span><span class="sxs-lookup"><span data-stu-id="42282-107">DESCRIPTION</span></span>
<span data-ttu-id="42282-108">네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 **AzEventhubName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="42282-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="42282-109">예제의</span><span class="sxs-lookup"><span data-stu-id="42282-109">EXAMPLES</span></span>

### <span data-ttu-id="42282-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="42282-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="42282-111">사용 가능한 경우 네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42282-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="42282-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="42282-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="42282-113">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 False로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42282-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="42282-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="42282-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="42282-115">사용 가능한 경우 ' MyNameSapceName ' 네임 스페이스에 대 한 별칭 이름 ' myAliasName '의 사용 가능 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42282-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="42282-116">변수</span><span class="sxs-lookup"><span data-stu-id="42282-116">PARAMETERS</span></span>

### <span data-ttu-id="42282-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="42282-117">-AliasName</span></span>
<span data-ttu-id="42282-118">DR 구성 이름-별칭 이름</span><span class="sxs-lookup"><span data-stu-id="42282-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="42282-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42282-119">-DefaultProfile</span></span>
<span data-ttu-id="42282-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42282-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42282-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="42282-121">-Namespace</span></span>
<span data-ttu-id="42282-122">Eventhub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="42282-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="42282-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42282-123">-ResourceGroupName</span></span>
<span data-ttu-id="42282-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="42282-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42282-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42282-125">CommonParameters</span></span>
<span data-ttu-id="42282-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42282-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42282-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42282-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42282-128">입력</span><span class="sxs-lookup"><span data-stu-id="42282-128">INPUTS</span></span>

### <span data-ttu-id="42282-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42282-129">System.String</span></span>

## <span data-ttu-id="42282-130">출력</span><span class="sxs-lookup"><span data-stu-id="42282-130">OUTPUTS</span></span>

### <span data-ttu-id="42282-131">PSCheckNameAvailabilityResultAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="42282-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="42282-132">상속자</span><span class="sxs-lookup"><span data-stu-id="42282-132">NOTES</span></span>

## <span data-ttu-id="42282-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42282-133">RELATED LINKS</span></span>
