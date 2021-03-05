---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: f88ff018f38040573783aff58287b4788017566a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996996"
---
# <span data-ttu-id="ea4b9-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ea4b9-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="ea4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4b9-103">리소스 그룹에서 Automation 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="ea4b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea4b9-104">SYNTAX</span></span>

### <span data-ttu-id="ea4b9-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="ea4b9-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea4b9-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ea4b9-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea4b9-107">설명</span><span class="sxs-lookup"><span data-stu-id="ea4b9-107">DESCRIPTION</span></span>
<span data-ttu-id="ea4b9-108">**Get-AzAutomationAccount** cmdlet은 리소스 그룹에서 Azure Automation 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="ea4b9-109">Automation 계정에 대한 자세한 내용은 New-AzAutomationAccount cmdlet을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="ea4b9-110">예제</span><span class="sxs-lookup"><span data-stu-id="ea4b9-110">EXAMPLES</span></span>

### <span data-ttu-id="ea4b9-111">예제 1: 모든 계정 사용</span><span class="sxs-lookup"><span data-stu-id="ea4b9-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="ea4b9-112">이 명령은 ResourceGroup03이라는 리소스 그룹의 모든 Automation 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="ea4b9-113">예제 2: 계정 사용</span><span class="sxs-lookup"><span data-stu-id="ea4b9-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="ea4b9-114">이 명령은 ContosoResourceGroup이라는 리소스 그룹에서 ContosoAutomationAccount이라는 Automation 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="ea4b9-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea4b9-115">PARAMETERS</span></span>

### <span data-ttu-id="ea4b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4b9-116">-DefaultProfile</span></span>
<span data-ttu-id="ea4b9-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ea4b9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea4b9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ea4b9-118">-Name</span></span>
<span data-ttu-id="ea4b9-119">이 cmdlet이 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="ea4b9-121">이 cmdlet에서 Automation 계정을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4b9-122">CommonParameters</span></span>
<span data-ttu-id="ea4b9-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4b9-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea4b9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4b9-125">입력</span><span class="sxs-lookup"><span data-stu-id="ea4b9-125">INPUTS</span></span>

### <span data-ttu-id="ea4b9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ea4b9-126">System.String</span></span>

## <span data-ttu-id="ea4b9-127">출력</span><span class="sxs-lookup"><span data-stu-id="ea4b9-127">OUTPUTS</span></span>

### <span data-ttu-id="ea4b9-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ea4b9-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ea4b9-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea4b9-129">NOTES</span></span>

## <span data-ttu-id="ea4b9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea4b9-130">RELATED LINKS</span></span>

[<span data-ttu-id="ea4b9-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ea4b9-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="ea4b9-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ea4b9-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="ea4b9-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ea4b9-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


