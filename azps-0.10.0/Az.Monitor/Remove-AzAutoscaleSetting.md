---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 1ae571eaaa401bc7d71ba93c5dadf93eaefc89ae
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875724"
---
# <span data-ttu-id="12ade-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="12ade-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="12ade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ade-102">SYNOPSIS</span></span>
<span data-ttu-id="12ade-103">자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="12ade-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12ade-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ade-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12ade-105">DESCRIPTION</span></span>
<span data-ttu-id="12ade-106">**AzAutoscaleSetting** Cmdlet은 자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="12ade-107">설정의 이름과이를 할당 받은 리소스 그룹의 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="12ade-108">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="12ade-109">예제의</span><span class="sxs-lookup"><span data-stu-id="12ade-109">EXAMPLES</span></span>

## <span data-ttu-id="12ade-110">변수</span><span class="sxs-lookup"><span data-stu-id="12ade-110">PARAMETERS</span></span>

### <span data-ttu-id="12ade-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ade-111">-DefaultProfile</span></span>
<span data-ttu-id="12ade-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="12ade-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12ade-113">-이름</span><span class="sxs-lookup"><span data-stu-id="12ade-113">-Name</span></span>
<span data-ttu-id="12ade-114">제거할 자동 크기 조정 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="12ade-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ade-115">-ResourceGroupName</span></span>
<span data-ttu-id="12ade-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="12ade-117">-확인</span><span class="sxs-lookup"><span data-stu-id="12ade-117">-Confirm</span></span>
<span data-ttu-id="12ade-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ade-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ade-119">-WhatIf</span></span>
<span data-ttu-id="12ade-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12ade-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ade-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ade-122">CommonParameters</span></span>
<span data-ttu-id="12ade-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ade-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ade-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="12ade-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ade-125">입력</span><span class="sxs-lookup"><span data-stu-id="12ade-125">INPUTS</span></span>

### <span data-ttu-id="12ade-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="12ade-126">System.String</span></span>

## <span data-ttu-id="12ade-127">출력</span><span class="sxs-lookup"><span data-stu-id="12ade-127">OUTPUTS</span></span>

### <span data-ttu-id="12ade-128">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="12ade-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="12ade-129">상속자</span><span class="sxs-lookup"><span data-stu-id="12ade-129">NOTES</span></span>

## <span data-ttu-id="12ade-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12ade-130">RELATED LINKS</span></span>

[<span data-ttu-id="12ade-131">추가-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="12ade-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="12ade-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="12ade-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


