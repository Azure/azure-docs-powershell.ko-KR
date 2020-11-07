---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: e960b1d68b57ef51ef51a6bd00365242e78f47a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697820"
---
# <span data-ttu-id="fd96c-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="fd96c-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="fd96c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd96c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd96c-103">Azure 자동화 소스 컨트롤의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="fd96c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd96c-104">SYNTAX</span></span>

### <span data-ttu-id="fd96c-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd96c-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd96c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fd96c-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd96c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd96c-107">DESCRIPTION</span></span>
<span data-ttu-id="fd96c-108">Get-AzAutomationSourceControl cmdlet은 자동화 소스 컨트롤을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="fd96c-109">특정 원본 컨트롤을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="fd96c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fd96c-110">EXAMPLES</span></span>

### <span data-ttu-id="fd96c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd96c-111">Example 1</span></span>
<span data-ttu-id="fd96c-112">이 명령은 devAccount 라는 계정에서 VSTSNative 이라는 자동화 원본 컨트롤을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="fd96c-113">변수</span><span class="sxs-lookup"><span data-stu-id="fd96c-113">PARAMETERS</span></span>

### <span data-ttu-id="fd96c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd96c-114">-AutomationAccountName</span></span>
<span data-ttu-id="fd96c-115">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-115">The automation account name.</span></span>

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

### <span data-ttu-id="fd96c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd96c-116">-DefaultProfile</span></span>
<span data-ttu-id="fd96c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd96c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="fd96c-118">-Name</span></span>
<span data-ttu-id="fd96c-119">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-119">The source control name.</span></span>

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

### <span data-ttu-id="fd96c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd96c-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd96c-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-121">The resource group name.</span></span>

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

### <span data-ttu-id="fd96c-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="fd96c-122">-SourceType</span></span>
<span data-ttu-id="fd96c-123">소스 컨트롤 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-123">The source control type.</span></span>

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

### <span data-ttu-id="fd96c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd96c-124">CommonParameters</span></span>
<span data-ttu-id="fd96c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd96c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd96c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd96c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd96c-127">입력</span><span class="sxs-lookup"><span data-stu-id="fd96c-127">INPUTS</span></span>

### <span data-ttu-id="fd96c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd96c-128">System.String</span></span>

## <span data-ttu-id="fd96c-129">출력</span><span class="sxs-lookup"><span data-stu-id="fd96c-129">OUTPUTS</span></span>

### <span data-ttu-id="fd96c-130">SourceControl를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="fd96c-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="fd96c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="fd96c-131">NOTES</span></span>

## <span data-ttu-id="fd96c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd96c-132">RELATED LINKS</span></span>
