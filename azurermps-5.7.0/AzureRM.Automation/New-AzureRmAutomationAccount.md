---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527136"
---
# <span data-ttu-id="ae92a-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ae92a-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="ae92a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae92a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae92a-103">Automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae92a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae92a-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae92a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae92a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae92a-106">**새 AzureRmAutomationAccount** cmdlet은 리소스 그룹에 Azure Automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="ae92a-107">Automation 계정은 다른 자동화 계정의 리소스에서 격리 된 자동화 리소스에 대 한 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="ae92a-108">자동화 리소스에는 runbook, 원하는 상태 구성 (DSC) 구성, 작업, 자산 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="ae92a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ae92a-109">EXAMPLES</span></span>

### <span data-ttu-id="ae92a-110">예제 1: automation 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="ae92a-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ae92a-111">이 명령은 동부 US 지역에 ContosoAutomationAccount 이라는 새 automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="ae92a-112">변수</span><span class="sxs-lookup"><span data-stu-id="ae92a-112">PARAMETERS</span></span>

### <span data-ttu-id="ae92a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae92a-113">-DefaultProfile</span></span>
<span data-ttu-id="ae92a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae92a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae92a-115">-위치</span><span class="sxs-lookup"><span data-stu-id="ae92a-115">-Location</span></span>
<span data-ttu-id="ae92a-116">이 cmdlet에서 자동화 계정을 만드는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="ae92a-117">유효한 위치를 얻으려면 Get-AzureRMLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae92a-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ae92a-118">-Name</span></span>
<span data-ttu-id="ae92a-119">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae92a-120">-계획</span><span class="sxs-lookup"><span data-stu-id="ae92a-120">-Plan</span></span>
<span data-ttu-id="ae92a-121">Automation 계정에 대 한 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="ae92a-122">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-122">Valid values are:</span></span>

- <span data-ttu-id="ae92a-123">기본적</span><span class="sxs-lookup"><span data-stu-id="ae92a-123">Basic</span></span>
- <span data-ttu-id="ae92a-124">비우거나</span><span class="sxs-lookup"><span data-stu-id="ae92a-124">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae92a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae92a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae92a-126">이 cmdlet이 Automation 계정을 추가 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae92a-127">태그</span><span class="sxs-lookup"><span data-stu-id="ae92a-127">-Tags</span></span>
<span data-ttu-id="ae92a-128">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae92a-129">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ae92a-129">For example:</span></span>

<span data-ttu-id="ae92a-130">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ae92a-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae92a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae92a-131">CommonParameters</span></span>
<span data-ttu-id="ae92a-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae92a-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae92a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae92a-134">입력</span><span class="sxs-lookup"><span data-stu-id="ae92a-134">INPUTS</span></span>

### <span data-ttu-id="ae92a-135">않아야</span><span class="sxs-lookup"><span data-stu-id="ae92a-135">None</span></span>
<span data-ttu-id="ae92a-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae92a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae92a-137">출력</span><span class="sxs-lookup"><span data-stu-id="ae92a-137">OUTPUTS</span></span>

### <span data-ttu-id="ae92a-138">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="ae92a-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ae92a-139">상속자</span><span class="sxs-lookup"><span data-stu-id="ae92a-139">NOTES</span></span>

## <span data-ttu-id="ae92a-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae92a-140">RELATED LINKS</span></span>

[<span data-ttu-id="ae92a-141">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ae92a-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="ae92a-142">제거-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ae92a-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="ae92a-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ae92a-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
