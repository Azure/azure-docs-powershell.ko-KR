---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: bbb90e728c9c43c011c4610ee47273af1fdae668
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531779"
---
# <span data-ttu-id="56ad1-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="56ad1-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="56ad1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="56ad1-103">Automation 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56ad1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56ad1-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56ad1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="56ad1-106">**Set-AzureRmAutomationAccount** Cmdlet은 Azure Automation 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="56ad1-107">자동화 계정에 대 한 자세한 내용은 New-AzureRmAutomationAccount cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="56ad1-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="56ad1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="56ad1-108">EXAMPLES</span></span>

### <span data-ttu-id="56ad1-109">예제 1: Automation 계정의 태그 설정</span><span class="sxs-lookup"><span data-stu-id="56ad1-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="56ad1-110">첫 번째 명령은 두 개의 키/값 쌍을 $Tags 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="56ad1-111">두 번째 명령은 AutomationAccount01 이라는 자동화 계정에 대 한 $Tags의 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="56ad1-112">예제 2: Automation 계정에 대 한 계획 변경</span><span class="sxs-lookup"><span data-stu-id="56ad1-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="56ad1-113">이 명령은 AutomationAccount01 이라는 Automation 계정에 대 한 계획을 기본으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="56ad1-114">변수</span><span class="sxs-lookup"><span data-stu-id="56ad1-114">PARAMETERS</span></span>

### <span data-ttu-id="56ad1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ad1-115">-DefaultProfile</span></span>
<span data-ttu-id="56ad1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="56ad1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56ad1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="56ad1-117">-Name</span></span>
<span data-ttu-id="56ad1-118">이 cmdlet이 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="56ad1-119">-계획</span><span class="sxs-lookup"><span data-stu-id="56ad1-119">-Plan</span></span>
<span data-ttu-id="56ad1-120">Automation 계정에 대 한 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="56ad1-121">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-121">Valid values are:</span></span>

- <span data-ttu-id="56ad1-122">기본적</span><span class="sxs-lookup"><span data-stu-id="56ad1-122">Basic</span></span>
- <span data-ttu-id="56ad1-123">비우거나</span><span class="sxs-lookup"><span data-stu-id="56ad1-123">Free</span></span>

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

### <span data-ttu-id="56ad1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ad1-124">-ResourceGroupName</span></span>
<span data-ttu-id="56ad1-125">이 cmdlet이 수정 하는 자동화 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="56ad1-126">태그</span><span class="sxs-lookup"><span data-stu-id="56ad1-126">-Tags</span></span>
<span data-ttu-id="56ad1-127">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="56ad1-128">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="56ad1-128">For example:</span></span>

<span data-ttu-id="56ad1-129">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="56ad1-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="56ad1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ad1-130">CommonParameters</span></span>
<span data-ttu-id="56ad1-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ad1-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ad1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ad1-133">입력</span><span class="sxs-lookup"><span data-stu-id="56ad1-133">INPUTS</span></span>

### <span data-ttu-id="56ad1-134">않아야</span><span class="sxs-lookup"><span data-stu-id="56ad1-134">None</span></span>
<span data-ttu-id="56ad1-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56ad1-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56ad1-136">출력</span><span class="sxs-lookup"><span data-stu-id="56ad1-136">OUTPUTS</span></span>

### <span data-ttu-id="56ad1-137">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="56ad1-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="56ad1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="56ad1-138">NOTES</span></span>

## <span data-ttu-id="56ad1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56ad1-139">RELATED LINKS</span></span>

[<span data-ttu-id="56ad1-140">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="56ad1-140">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="56ad1-141">새로운 AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="56ad1-141">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="56ad1-142">제거-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="56ad1-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)