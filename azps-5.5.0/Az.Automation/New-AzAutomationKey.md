---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201068"
---
# <span data-ttu-id="90490-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="90490-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="90490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90490-102">SYNOPSIS</span></span>
<span data-ttu-id="90490-103">Automation 계정에 대한 등록 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="90490-104">구문</span><span class="sxs-lookup"><span data-stu-id="90490-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90490-105">설명</span><span class="sxs-lookup"><span data-stu-id="90490-105">DESCRIPTION</span></span>
<span data-ttu-id="90490-106">**New-AzAutomationKey** cmdlet은 Azure Automation 계정에 대한 등록 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="90490-107">예제</span><span class="sxs-lookup"><span data-stu-id="90490-107">EXAMPLES</span></span>

### <span data-ttu-id="90490-108">예제 1: Automation 계정에 대한 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="90490-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="90490-109">이 명령은 ResourceGroup01이라는 리소스 그룹에 AutomationAccount01이라는 Azure Automation 계정에 대한 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="90490-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90490-110">PARAMETERS</span></span>

### <span data-ttu-id="90490-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90490-111">-AutomationAccountName</span></span>
<span data-ttu-id="90490-112">이 cmdlet이 키를 다시 생성하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="90490-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90490-113">-DefaultProfile</span></span>
<span data-ttu-id="90490-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90490-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90490-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="90490-115">-KeyType</span></span>
<span data-ttu-id="90490-116">에이전트 등록 키의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="90490-117">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="90490-117">Valid values are:</span></span> 
- <span data-ttu-id="90490-118">기본</span><span class="sxs-lookup"><span data-stu-id="90490-118">Primary</span></span> 
- <span data-ttu-id="90490-119">보조</span><span class="sxs-lookup"><span data-stu-id="90490-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90490-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90490-120">-ResourceGroupName</span></span>
<span data-ttu-id="90490-121">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="90490-122">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 Automation 계정에 대한 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="90490-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90490-123">CommonParameters</span></span>
<span data-ttu-id="90490-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90490-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90490-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="90490-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90490-126">입력</span><span class="sxs-lookup"><span data-stu-id="90490-126">INPUTS</span></span>

### <span data-ttu-id="90490-127">System.String</span><span class="sxs-lookup"><span data-stu-id="90490-127">System.String</span></span>

## <span data-ttu-id="90490-128">출력</span><span class="sxs-lookup"><span data-stu-id="90490-128">OUTPUTS</span></span>

### <span data-ttu-id="90490-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="90490-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="90490-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90490-130">NOTES</span></span>

## <span data-ttu-id="90490-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90490-131">RELATED LINKS</span></span>
