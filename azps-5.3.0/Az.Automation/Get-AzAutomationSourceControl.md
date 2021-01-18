---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494307"
---
# <span data-ttu-id="0a34e-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="0a34e-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="0a34e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a34e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a34e-103">Azure Automation 원본 제어 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="0a34e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a34e-104">SYNTAX</span></span>

### <span data-ttu-id="0a34e-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a34e-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a34e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0a34e-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a34e-107">설명</span><span class="sxs-lookup"><span data-stu-id="0a34e-107">DESCRIPTION</span></span>
<span data-ttu-id="0a34e-108">Get-AzAutomationSourceControl cmdlet은 Automation 원본 제어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="0a34e-109">특정 소스 제어를 얻습니다. 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="0a34e-110">예제</span><span class="sxs-lookup"><span data-stu-id="0a34e-110">EXAMPLES</span></span>

### <span data-ttu-id="0a34e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a34e-111">Example 1</span></span>
<span data-ttu-id="0a34e-112">이 명령은 devAccount라는 계정에서 VSTSNative라는 Automation 소스 제어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="0a34e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a34e-113">PARAMETERS</span></span>

### <span data-ttu-id="0a34e-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a34e-114">-AutomationAccountName</span></span>
<span data-ttu-id="0a34e-115">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-115">The automation account name.</span></span>

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

### <span data-ttu-id="0a34e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a34e-116">-DefaultProfile</span></span>
<span data-ttu-id="0a34e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a34e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0a34e-118">-Name</span></span>
<span data-ttu-id="0a34e-119">원본 제어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a34e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a34e-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a34e-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-121">The resource group name.</span></span>

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

### <span data-ttu-id="0a34e-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="0a34e-122">-SourceType</span></span>
<span data-ttu-id="0a34e-123">원본 제어 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a34e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a34e-124">CommonParameters</span></span>
<span data-ttu-id="0a34e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a34e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a34e-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a34e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a34e-127">입력</span><span class="sxs-lookup"><span data-stu-id="0a34e-127">INPUTS</span></span>

### <span data-ttu-id="0a34e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0a34e-128">System.String</span></span>

## <span data-ttu-id="0a34e-129">출력</span><span class="sxs-lookup"><span data-stu-id="0a34e-129">OUTPUTS</span></span>

### <span data-ttu-id="0a34e-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="0a34e-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="0a34e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a34e-131">NOTES</span></span>

## <span data-ttu-id="0a34e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a34e-132">RELATED LINKS</span></span>
