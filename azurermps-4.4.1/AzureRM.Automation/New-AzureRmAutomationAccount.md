---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702884"
---
# <span data-ttu-id="c6291-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c6291-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="c6291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6291-102">SYNOPSIS</span></span>
<span data-ttu-id="c6291-103">Automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6291-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6291-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6291-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6291-105">DESCRIPTION</span></span>
<span data-ttu-id="c6291-106">**새 AzureRmAutomationAccount** cmdlet은 리소스 그룹에 Azure Automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="c6291-107">Automation 계정은 다른 자동화 계정의 리소스에서 격리 된 자동화 리소스에 대 한 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="c6291-108">자동화 리소스에는 runbook, 원하는 상태 구성 (DSC) 구성, 작업, 자산 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="c6291-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c6291-109">EXAMPLES</span></span>

### <span data-ttu-id="c6291-110">예제 1: automation 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="c6291-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c6291-111">이 명령은 동부 US 지역에 ContosoAutomationAccount 이라는 새 automation 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="c6291-112">변수</span><span class="sxs-lookup"><span data-stu-id="c6291-112">PARAMETERS</span></span>

### <span data-ttu-id="c6291-113">-위치</span><span class="sxs-lookup"><span data-stu-id="c6291-113">-Location</span></span>
<span data-ttu-id="c6291-114">이 cmdlet에서 자동화 계정을 만드는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="c6291-115">유효한 위치를 얻으려면 Get-AzureRMLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="c6291-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c6291-116">-Name</span></span>
<span data-ttu-id="c6291-117">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="c6291-118">-계획</span><span class="sxs-lookup"><span data-stu-id="c6291-118">-Plan</span></span>
<span data-ttu-id="c6291-119">Automation 계정에 대 한 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="c6291-120">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-120">Valid values are:</span></span>

- <span data-ttu-id="c6291-121">기본적</span><span class="sxs-lookup"><span data-stu-id="c6291-121">Basic</span></span>
- <span data-ttu-id="c6291-122">비우거나</span><span class="sxs-lookup"><span data-stu-id="c6291-122">Free</span></span>

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

### <span data-ttu-id="c6291-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6291-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6291-124">이 cmdlet이 Automation 계정을 추가 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="c6291-125">태그</span><span class="sxs-lookup"><span data-stu-id="c6291-125">-Tags</span></span>
<span data-ttu-id="c6291-126">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c6291-127">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c6291-127">For example:</span></span>

<span data-ttu-id="c6291-128">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c6291-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c6291-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6291-129">-DefaultProfile</span></span>
<span data-ttu-id="c6291-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6291-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6291-131">CommonParameters</span></span>
<span data-ttu-id="c6291-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6291-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6291-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6291-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6291-134">입력</span><span class="sxs-lookup"><span data-stu-id="c6291-134">INPUTS</span></span>

## <span data-ttu-id="c6291-135">출력</span><span class="sxs-lookup"><span data-stu-id="c6291-135">OUTPUTS</span></span>

### <span data-ttu-id="c6291-136">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="c6291-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="c6291-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c6291-137">NOTES</span></span>

## <span data-ttu-id="c6291-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6291-138">RELATED LINKS</span></span>

[<span data-ttu-id="c6291-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c6291-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="c6291-140">제거-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c6291-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="c6291-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c6291-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
