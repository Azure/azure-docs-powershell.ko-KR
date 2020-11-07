---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881529"
---
# <span data-ttu-id="32bbb-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="32bbb-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="32bbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="32bbb-103">자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32bbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32bbb-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32bbb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="32bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="32bbb-106">**AzureRmAutoscaleSetting** Cmdlet은 자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="32bbb-107">설정의 이름과이를 할당 받은 리소스 그룹의 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="32bbb-108">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="32bbb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="32bbb-109">EXAMPLES</span></span>

## <span data-ttu-id="32bbb-110">변수</span><span class="sxs-lookup"><span data-stu-id="32bbb-110">PARAMETERS</span></span>

### <span data-ttu-id="32bbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bbb-111">-DefaultProfile</span></span>
<span data-ttu-id="32bbb-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="32bbb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32bbb-113">-이름</span><span class="sxs-lookup"><span data-stu-id="32bbb-113">-Name</span></span>
<span data-ttu-id="32bbb-114">제거할 자동 크기 조정 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="32bbb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bbb-115">-ResourceGroupName</span></span>
<span data-ttu-id="32bbb-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bbb-117">-확인</span><span class="sxs-lookup"><span data-stu-id="32bbb-117">-Confirm</span></span>
<span data-ttu-id="32bbb-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32bbb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bbb-119">-WhatIf</span></span>
<span data-ttu-id="32bbb-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32bbb-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32bbb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bbb-122">CommonParameters</span></span>
<span data-ttu-id="32bbb-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32bbb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bbb-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32bbb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bbb-125">입력</span><span class="sxs-lookup"><span data-stu-id="32bbb-125">INPUTS</span></span>

### <span data-ttu-id="32bbb-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32bbb-126">System.String</span></span>

## <span data-ttu-id="32bbb-127">출력</span><span class="sxs-lookup"><span data-stu-id="32bbb-127">OUTPUTS</span></span>

### <span data-ttu-id="32bbb-128">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="32bbb-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="32bbb-129">상속자</span><span class="sxs-lookup"><span data-stu-id="32bbb-129">NOTES</span></span>

## <span data-ttu-id="32bbb-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32bbb-130">RELATED LINKS</span></span>

[<span data-ttu-id="32bbb-131">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="32bbb-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="32bbb-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="32bbb-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


