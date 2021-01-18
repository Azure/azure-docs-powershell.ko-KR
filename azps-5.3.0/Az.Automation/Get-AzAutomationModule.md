---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494323"
---
# <span data-ttu-id="b7e4b-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b7e4b-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="b7e4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e4b-103">Automation에서 모듈에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="b7e4b-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7e4b-104">SYNTAX</span></span>

### <span data-ttu-id="b7e4b-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7e4b-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7e4b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b7e4b-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7e4b-107">설명</span><span class="sxs-lookup"><span data-stu-id="b7e4b-107">DESCRIPTION</span></span>
<span data-ttu-id="b7e4b-108">**Get-AzAutomationModule** cmdlet은 Azure Automation에서 모듈에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="b7e4b-109">예제</span><span class="sxs-lookup"><span data-stu-id="b7e4b-109">EXAMPLES</span></span>

### <span data-ttu-id="b7e4b-110">예제 1: 모든 모듈을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b7e4b-111">이 명령은 Contoso17이라는 Automation 계정의 모든 모듈을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b7e4b-112">예제 2: 모듈 얻기</span><span class="sxs-lookup"><span data-stu-id="b7e4b-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b7e4b-113">이 명령은 Contoso17이라는 Automation 계정에서 ContosoModule이라는 모듈을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b7e4b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7e4b-114">PARAMETERS</span></span>

### <span data-ttu-id="b7e4b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b7e4b-115">-AutomationAccountName</span></span>
<span data-ttu-id="b7e4b-116">이 cmdlet이 모듈 메타데이터를 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="b7e4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4b-117">-DefaultProfile</span></span>
<span data-ttu-id="b7e4b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b7e4b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7e4b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7e4b-119">-Name</span></span>
<span data-ttu-id="b7e4b-120">이 cmdlet이 메타데이터를 얻을 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e4b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e4b-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7e4b-122">이 cmdlet이 모듈 메타데이터를 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="b7e4b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e4b-123">CommonParameters</span></span>
<span data-ttu-id="b7e4b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e4b-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b7e4b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e4b-126">입력</span><span class="sxs-lookup"><span data-stu-id="b7e4b-126">INPUTS</span></span>

### <span data-ttu-id="b7e4b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b7e4b-127">System.String</span></span>

## <span data-ttu-id="b7e4b-128">출력</span><span class="sxs-lookup"><span data-stu-id="b7e4b-128">OUTPUTS</span></span>

### <span data-ttu-id="b7e4b-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="b7e4b-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="b7e4b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7e4b-130">NOTES</span></span>

## <span data-ttu-id="b7e4b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7e4b-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7e4b-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b7e4b-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="b7e4b-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b7e4b-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="b7e4b-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b7e4b-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


