---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 978e1bf2e826e576745748c43249bf8257f129cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014304"
---
# <span data-ttu-id="02801-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02801-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="02801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02801-102">SYNOPSIS</span></span>
<span data-ttu-id="02801-103">Automation에서 모듈에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="02801-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="02801-104">구문</span><span class="sxs-lookup"><span data-stu-id="02801-104">SYNTAX</span></span>

### <span data-ttu-id="02801-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="02801-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02801-106">ByName</span><span class="sxs-lookup"><span data-stu-id="02801-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02801-107">설명</span><span class="sxs-lookup"><span data-stu-id="02801-107">DESCRIPTION</span></span>
<span data-ttu-id="02801-108">**Get-AzAutomationModule** cmdlet은 Azure Automation의 모듈에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="02801-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="02801-109">예제</span><span class="sxs-lookup"><span data-stu-id="02801-109">EXAMPLES</span></span>

### <span data-ttu-id="02801-110">예제 1: 모든 모듈을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="02801-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="02801-111">이 명령은 Contoso17이라는 Automation 계정의 모든 모듈을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="02801-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="02801-112">예제 2: 모듈 얻기</span><span class="sxs-lookup"><span data-stu-id="02801-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="02801-113">이 명령은 Contoso17이라는 Automation 계정에서 ContosoModule이라는 모듈을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="02801-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="02801-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="02801-114">PARAMETERS</span></span>

### <span data-ttu-id="02801-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02801-115">-AutomationAccountName</span></span>
<span data-ttu-id="02801-116">이 cmdlet에서 모듈 메타데이터를 얻을 수 있는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02801-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="02801-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02801-117">-DefaultProfile</span></span>
<span data-ttu-id="02801-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="02801-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02801-119">-Name</span><span class="sxs-lookup"><span data-stu-id="02801-119">-Name</span></span>
<span data-ttu-id="02801-120">이 cmdlet에서 메타데이터를 얻을 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02801-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="02801-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02801-121">-ResourceGroupName</span></span>
<span data-ttu-id="02801-122">이 cmdlet에서 모듈 메타데이터를 얻을 수 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02801-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="02801-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02801-123">CommonParameters</span></span>
<span data-ttu-id="02801-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02801-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02801-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="02801-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02801-126">입력</span><span class="sxs-lookup"><span data-stu-id="02801-126">INPUTS</span></span>

### <span data-ttu-id="02801-127">System.String</span><span class="sxs-lookup"><span data-stu-id="02801-127">System.String</span></span>

## <span data-ttu-id="02801-128">출력</span><span class="sxs-lookup"><span data-stu-id="02801-128">OUTPUTS</span></span>

### <span data-ttu-id="02801-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="02801-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="02801-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02801-130">NOTES</span></span>

## <span data-ttu-id="02801-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02801-131">RELATED LINKS</span></span>

[<span data-ttu-id="02801-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02801-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="02801-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02801-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="02801-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02801-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


