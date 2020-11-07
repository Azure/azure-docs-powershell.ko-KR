---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697805"
---
# <span data-ttu-id="eace3-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eace3-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="eace3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eace3-102">SYNOPSIS</span></span>
<span data-ttu-id="eace3-103">Automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-103">Creates an Automation account.</span></span>

## <span data-ttu-id="eace3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eace3-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eace3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eace3-105">DESCRIPTION</span></span>
<span data-ttu-id="eace3-106">**새 AzAutomationAccount** cmdlet은 리소스 그룹에 Azure Automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="eace3-107">Automation 계정은 다른 자동화 계정의 리소스에서 격리 된 자동화 리소스에 대 한 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="eace3-108">자동화 리소스에는 runbook, 원하는 상태 구성 (DSC) 구성, 작업, 자산 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="eace3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eace3-109">EXAMPLES</span></span>

### <span data-ttu-id="eace3-110">예제 1: automation 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="eace3-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eace3-111">이 명령은 동부 US 지역에 ContosoAutomationAccount 이라는 새 automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="eace3-112">변수</span><span class="sxs-lookup"><span data-stu-id="eace3-112">PARAMETERS</span></span>

### <span data-ttu-id="eace3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eace3-113">-DefaultProfile</span></span>
<span data-ttu-id="eace3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eace3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eace3-115">-위치</span><span class="sxs-lookup"><span data-stu-id="eace3-115">-Location</span></span>
<span data-ttu-id="eace3-116">이 cmdlet에서 자동화 계정을 만드는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="eace3-117">유효한 위치를 얻으려면 Get-AzLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eace3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="eace3-118">-Name</span></span>
<span data-ttu-id="eace3-119">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eace3-120">-계획</span><span class="sxs-lookup"><span data-stu-id="eace3-120">-Plan</span></span>
<span data-ttu-id="eace3-121">Automation 계정에 대 한 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="eace3-122">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-122">Valid values are:</span></span>
- <span data-ttu-id="eace3-123">기본적</span><span class="sxs-lookup"><span data-stu-id="eace3-123">Basic</span></span>
- <span data-ttu-id="eace3-124">비우거나</span><span class="sxs-lookup"><span data-stu-id="eace3-124">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eace3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eace3-125">-ResourceGroupName</span></span>
<span data-ttu-id="eace3-126">이 cmdlet이 Automation 계정을 추가 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="eace3-127">태그</span><span class="sxs-lookup"><span data-stu-id="eace3-127">-Tags</span></span>
<span data-ttu-id="eace3-128">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eace3-129">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eace3-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eace3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eace3-130">CommonParameters</span></span>
<span data-ttu-id="eace3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eace3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eace3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eace3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eace3-133">입력</span><span class="sxs-lookup"><span data-stu-id="eace3-133">INPUTS</span></span>

### <span data-ttu-id="eace3-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eace3-134">System.String</span></span>

### <span data-ttu-id="eace3-135">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="eace3-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="eace3-136">출력</span><span class="sxs-lookup"><span data-stu-id="eace3-136">OUTPUTS</span></span>

### <span data-ttu-id="eace3-137">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="eace3-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="eace3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="eace3-138">NOTES</span></span>

## <span data-ttu-id="eace3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eace3-139">RELATED LINKS</span></span>

[<span data-ttu-id="eace3-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eace3-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="eace3-141">제거-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eace3-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="eace3-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eace3-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
