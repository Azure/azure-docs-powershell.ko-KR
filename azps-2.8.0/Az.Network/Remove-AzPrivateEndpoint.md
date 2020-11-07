---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 1ad9ff225871cde9104a346bd758f2716f630bc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869689"
---
# <span data-ttu-id="44b6b-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b6b-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="44b6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="44b6b-103">개인 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="44b6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44b6b-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="44b6b-106">**AzPrivateEndpoint** cmdlet은 개인 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="44b6b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44b6b-107">EXAMPLES</span></span>

### <span data-ttu-id="44b6b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="44b6b-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="44b6b-109">이 예제에서는 MyPrivateEndpoint1 라는 개인 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="44b6b-110">변수</span><span class="sxs-lookup"><span data-stu-id="44b6b-110">PARAMETERS</span></span>

### <span data-ttu-id="44b6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44b6b-111">-AsJob</span></span>
<span data-ttu-id="44b6b-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="44b6b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44b6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b6b-113">-DefaultProfile</span></span>
<span data-ttu-id="44b6b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44b6b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="44b6b-115">-Force</span></span>
<span data-ttu-id="44b6b-116">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="44b6b-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="44b6b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="44b6b-117">-Name</span></span>
<span data-ttu-id="44b6b-118">개인 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b6b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44b6b-119">-PassThru</span></span>
<span data-ttu-id="44b6b-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="44b6b-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44b6b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b6b-122">-ResourceGroupName</span></span>
<span data-ttu-id="44b6b-123">개인 끝점의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-123">The resource group name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b6b-124">-확인</span><span class="sxs-lookup"><span data-stu-id="44b6b-124">-Confirm</span></span>
<span data-ttu-id="44b6b-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b6b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b6b-126">-WhatIf</span></span>
<span data-ttu-id="44b6b-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b6b-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b6b-129">CommonParameters</span></span>
<span data-ttu-id="44b6b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b6b-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="44b6b-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b6b-132">입력</span><span class="sxs-lookup"><span data-stu-id="44b6b-132">INPUTS</span></span>

### <span data-ttu-id="44b6b-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44b6b-133">System.String</span></span>

## <span data-ttu-id="44b6b-134">출력</span><span class="sxs-lookup"><span data-stu-id="44b6b-134">OUTPUTS</span></span>

### <span data-ttu-id="44b6b-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="44b6b-135">System.Boolean</span></span>

## <span data-ttu-id="44b6b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="44b6b-136">NOTES</span></span>

## <span data-ttu-id="44b6b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44b6b-137">RELATED LINKS</span></span>

[<span data-ttu-id="44b6b-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b6b-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="44b6b-139">새로운 AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b6b-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)