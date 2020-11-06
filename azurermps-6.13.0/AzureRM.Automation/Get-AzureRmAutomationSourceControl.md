---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 3e7affd09e8c24c1d3c1759e78ea09a0c849ff32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533448"
---
# <span data-ttu-id="ee1c7-101">Get-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="ee1c7-101">Get-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="ee1c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1c7-103">Azure 자동화 소스 컨트롤의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-103">Gets a list of Azure Automation source controls.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee1c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee1c7-104">SYNTAX</span></span>

### <span data-ttu-id="ee1c7-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="ee1c7-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee1c7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ee1c7-106">ByName</span></span>
```
Get-AzureRmAutomationSourceControl -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee1c7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ee1c7-107">DESCRIPTION</span></span>
<span data-ttu-id="ee1c7-108">Get-AzureRmAutomationSourceControl cmdlet은 자동화 소스 컨트롤을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-108">The Get-AzureRmAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="ee1c7-109">특정 원본 컨트롤을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="ee1c7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ee1c7-110">EXAMPLES</span></span>

### <span data-ttu-id="ee1c7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee1c7-111">Example 1</span></span>
<span data-ttu-id="ee1c7-112">이 명령은 devAccount 라는 계정에서 VSTSNative 이라는 자동화 원본 컨트롤을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="ee1c7-113">변수</span><span class="sxs-lookup"><span data-stu-id="ee1c7-113">PARAMETERS</span></span>

### <span data-ttu-id="ee1c7-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee1c7-114">-AutomationAccountName</span></span>
<span data-ttu-id="ee1c7-115">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-115">The automation account name.</span></span>

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

### <span data-ttu-id="ee1c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1c7-116">-DefaultProfile</span></span>
<span data-ttu-id="ee1c7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1c7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ee1c7-118">-Name</span></span>
<span data-ttu-id="ee1c7-119">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-119">The source control name.</span></span>

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

### <span data-ttu-id="ee1c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee1c7-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-121">The resource group name.</span></span>

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

### <span data-ttu-id="ee1c7-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="ee1c7-122">-SourceType</span></span>
<span data-ttu-id="ee1c7-123">소스 컨트롤 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-123">The source control type.</span></span>

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

### <span data-ttu-id="ee1c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1c7-124">CommonParameters</span></span>
<span data-ttu-id="ee1c7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1c7-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1c7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1c7-127">입력</span><span class="sxs-lookup"><span data-stu-id="ee1c7-127">INPUTS</span></span>

### <span data-ttu-id="ee1c7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee1c7-128">System.String</span></span>

## <span data-ttu-id="ee1c7-129">출력</span><span class="sxs-lookup"><span data-stu-id="ee1c7-129">OUTPUTS</span></span>

### <span data-ttu-id="ee1c7-130">SourceControl를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="ee1c7-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ee1c7-131">NOTES</span></span>

## <span data-ttu-id="ee1c7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee1c7-132">RELATED LINKS</span></span>
