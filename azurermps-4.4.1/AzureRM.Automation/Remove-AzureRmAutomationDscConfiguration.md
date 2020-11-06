---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531209"
---
# <span data-ttu-id="9bc02-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bc02-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="9bc02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc02-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc02-103">자동화에서 DSC 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bc02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9bc02-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bc02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9bc02-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc02-106">**AzureRmAutomationDscConfiguration** Cmdlet은 Azure 자동화에서 APS (원하는 상태 구성) 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="9bc02-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9bc02-107">EXAMPLES</span></span>

## <span data-ttu-id="9bc02-108">변수</span><span class="sxs-lookup"><span data-stu-id="9bc02-108">PARAMETERS</span></span>

### <span data-ttu-id="9bc02-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9bc02-109">-AutomationAccountName</span></span>
<span data-ttu-id="9bc02-110">이 cmdlet이 제거 하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc02-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9bc02-111">-Force</span></span>
<span data-ttu-id="9bc02-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="9bc02-112">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc02-113">-이름</span><span class="sxs-lookup"><span data-stu-id="9bc02-113">-Name</span></span>
<span data-ttu-id="9bc02-114">이 cmdlet이 제거 하는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc02-115">-ResourceGroupName</span></span>
<span data-ttu-id="9bc02-116">이 cmdlet에서 DSC 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="9bc02-117">-확인</span><span class="sxs-lookup"><span data-stu-id="9bc02-117">-Confirm</span></span>
<span data-ttu-id="9bc02-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc02-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc02-119">-WhatIf</span></span>
<span data-ttu-id="9bc02-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bc02-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc02-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc02-122">-DefaultProfile</span></span>
<span data-ttu-id="9bc02-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bc02-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc02-124">CommonParameters</span></span>
<span data-ttu-id="9bc02-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc02-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc02-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc02-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc02-127">입력</span><span class="sxs-lookup"><span data-stu-id="9bc02-127">INPUTS</span></span>

## <span data-ttu-id="9bc02-128">출력</span><span class="sxs-lookup"><span data-stu-id="9bc02-128">OUTPUTS</span></span>

## <span data-ttu-id="9bc02-129">상속자</span><span class="sxs-lookup"><span data-stu-id="9bc02-129">NOTES</span></span>

## <span data-ttu-id="9bc02-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bc02-130">RELATED LINKS</span></span>

[<span data-ttu-id="9bc02-131">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bc02-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9bc02-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bc02-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9bc02-133">가져오기-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bc02-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


