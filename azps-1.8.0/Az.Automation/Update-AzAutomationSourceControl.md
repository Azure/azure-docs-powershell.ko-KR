---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: 7786431232f9570557593d2fbdde65a21e34f9bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701478"
---
# <span data-ttu-id="645bb-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="645bb-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="645bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="645bb-102">SYNOPSIS</span></span>
<span data-ttu-id="645bb-103">Azure Automation 원본 컨트롤을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="645bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="645bb-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="645bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="645bb-105">DESCRIPTION</span></span>
<span data-ttu-id="645bb-106">Update-AzAutomationSourceControl cmdlet은 Azure Automation에서 원본 컨트롤의 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="645bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="645bb-107">EXAMPLES</span></span>

### <span data-ttu-id="645bb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="645bb-108">Example 1</span></span>
<span data-ttu-id="645bb-109">이 명령은 devAccount 라는 계정에서 VSTSNative 이라는 Azure Automation 원본 컨트롤에 대해 없음 Runbook 필드를 false로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="645bb-110">변수</span><span class="sxs-lookup"><span data-stu-id="645bb-110">PARAMETERS</span></span>

### <span data-ttu-id="645bb-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="645bb-111">-AccessToken</span></span>
<span data-ttu-id="645bb-112">소스 제어 액세스 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645bb-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="645bb-113">-AutomationAccountName</span></span>
<span data-ttu-id="645bb-114">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-114">The automation account name.</span></span>

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

### <span data-ttu-id="645bb-115">-AutoSync</span><span class="sxs-lookup"><span data-stu-id="645bb-115">-AutoSync</span></span>
<span data-ttu-id="645bb-116">원본 컨트롤에 대 한 autoSync 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645bb-117">-분기</span><span class="sxs-lookup"><span data-stu-id="645bb-117">-Branch</span></span>
<span data-ttu-id="645bb-118">소스 제어 분기입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-118">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645bb-119">-DefaultProfile</span></span>
<span data-ttu-id="645bb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="645bb-121">-설명</span><span class="sxs-lookup"><span data-stu-id="645bb-121">-Description</span></span>
<span data-ttu-id="645bb-122">소스 제어 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-122">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645bb-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="645bb-123">-FolderPath</span></span>
<span data-ttu-id="645bb-124">소스 제어 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-124">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645bb-125">-이름</span><span class="sxs-lookup"><span data-stu-id="645bb-125">-Name</span></span>
<span data-ttu-id="645bb-126">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-126">The source control name.</span></span>

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

### <span data-ttu-id="645bb-127">-없음 Runbook</span><span class="sxs-lookup"><span data-stu-id="645bb-127">-PublishRunbook</span></span>
<span data-ttu-id="645bb-128">원본 컨트롤의 # Runbook 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645bb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="645bb-129">-ResourceGroupName</span></span>
<span data-ttu-id="645bb-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-130">The resource group name.</span></span>

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

### <span data-ttu-id="645bb-131">-확인</span><span class="sxs-lookup"><span data-stu-id="645bb-131">-Confirm</span></span>
<span data-ttu-id="645bb-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="645bb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="645bb-133">-WhatIf</span></span>
<span data-ttu-id="645bb-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="645bb-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="645bb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645bb-136">CommonParameters</span></span>
<span data-ttu-id="645bb-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="645bb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645bb-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645bb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645bb-139">입력</span><span class="sxs-lookup"><span data-stu-id="645bb-139">INPUTS</span></span>

### <span data-ttu-id="645bb-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="645bb-140">System.String</span></span>

## <span data-ttu-id="645bb-141">출력</span><span class="sxs-lookup"><span data-stu-id="645bb-141">OUTPUTS</span></span>

### <span data-ttu-id="645bb-142">SourceControl를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="645bb-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="645bb-143">상속자</span><span class="sxs-lookup"><span data-stu-id="645bb-143">NOTES</span></span>

## <span data-ttu-id="645bb-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="645bb-144">RELATED LINKS</span></span>
