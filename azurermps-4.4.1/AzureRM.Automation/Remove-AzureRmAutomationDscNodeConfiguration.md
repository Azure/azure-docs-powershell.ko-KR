---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 56ceba33845061af4e0ccdf3247bab16e079e90c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531208"
---
# <span data-ttu-id="a0f7c-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f7c-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="a0f7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f7c-103">자동화의 DSC 노드 구성에서 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0f7c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f7c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a0f7c-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f7c-106">**AzureRmAutomationDscNodeConfiguration** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 노드 구성에서 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="a0f7c-107">자동화는 DSC 노드 구성을 MOF (관리 개체 형식) 구성 문서로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="a0f7c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a0f7c-108">EXAMPLES</span></span>

## <span data-ttu-id="a0f7c-109">변수</span><span class="sxs-lookup"><span data-stu-id="a0f7c-109">PARAMETERS</span></span>

### <span data-ttu-id="a0f7c-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0f7c-110">-AutomationAccountName</span></span>
<span data-ttu-id="a0f7c-111">이 cmdlet이 메타 데이터를 제거 하는 DSC 노드 구성을 포함 하는 자동화 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="a0f7c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a0f7c-112">-Force</span></span>
<span data-ttu-id="a0f7c-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="a0f7c-113">ps_force</span></span>

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

### <span data-ttu-id="a0f7c-114">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="a0f7c-114">-IgnoreNodeMappings</span></span>
<span data-ttu-id="a0f7c-115">이 cmdlet이 노드 매핑을 무시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-115">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f7c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a0f7c-116">-Name</span></span>
<span data-ttu-id="a0f7c-117">이 cmdlet이 메타 데이터를 제거 하는 DSC 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-117">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f7c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f7c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0f7c-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a0f7c-120">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 DSC 노드 구성에 대 한 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-120">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0f7c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="a0f7c-121">-Confirm</span></span>
<span data-ttu-id="a0f7c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f7c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f7c-123">-WhatIf</span></span>
<span data-ttu-id="a0f7c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f7c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f7c-126">-DefaultProfile</span></span>
<span data-ttu-id="a0f7c-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0f7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f7c-128">CommonParameters</span></span>
<span data-ttu-id="a0f7c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f7c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f7c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f7c-131">입력</span><span class="sxs-lookup"><span data-stu-id="a0f7c-131">INPUTS</span></span>

## <span data-ttu-id="a0f7c-132">출력</span><span class="sxs-lookup"><span data-stu-id="a0f7c-132">OUTPUTS</span></span>

## <span data-ttu-id="a0f7c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a0f7c-133">NOTES</span></span>

## <span data-ttu-id="a0f7c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0f7c-134">RELATED LINKS</span></span>

[<span data-ttu-id="a0f7c-135">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f7c-135">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a0f7c-136">가져오기-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f7c-136">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a0f7c-137">Azure 자동화 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0f7c-137">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


