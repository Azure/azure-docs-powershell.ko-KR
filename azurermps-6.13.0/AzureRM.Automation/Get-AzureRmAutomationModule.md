---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2ed40d0ee0698c8e0ee8d4a1c443db32c843ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701991"
---
# <span data-ttu-id="2d127-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2d127-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="2d127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d127-102">SYNOPSIS</span></span>
<span data-ttu-id="2d127-103">자동화에서 모듈에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d127-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d127-104">SYNTAX</span></span>

### <span data-ttu-id="2d127-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d127-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d127-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2d127-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d127-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2d127-107">DESCRIPTION</span></span>
<span data-ttu-id="2d127-108">**AzureRmAutomationModule** Cmdlet은 Azure 자동화에서 모듈에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="2d127-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2d127-109">EXAMPLES</span></span>

### <span data-ttu-id="2d127-110">예제 1: 모든 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="2d127-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2d127-111">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="2d127-112">예제 2: 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="2d127-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2d127-113">이 명령은 Contoso17 이라는 Automation 계정의 ContosoModule 라는 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="2d127-114">변수</span><span class="sxs-lookup"><span data-stu-id="2d127-114">PARAMETERS</span></span>

### <span data-ttu-id="2d127-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d127-115">-AutomationAccountName</span></span>
<span data-ttu-id="2d127-116">이 cmdlet이 모듈 메타 데이터를 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="2d127-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d127-117">-DefaultProfile</span></span>
<span data-ttu-id="2d127-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2d127-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d127-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2d127-119">-Name</span></span>
<span data-ttu-id="2d127-120">이 cmdlet이 메타 데이터를 가져오는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d127-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d127-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d127-122">이 cmdlet이 모듈 메타 데이터를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="2d127-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d127-123">CommonParameters</span></span>
<span data-ttu-id="2d127-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d127-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d127-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d127-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d127-126">입력</span><span class="sxs-lookup"><span data-stu-id="2d127-126">INPUTS</span></span>

### <span data-ttu-id="2d127-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d127-127">System.String</span></span>

## <span data-ttu-id="2d127-128">출력</span><span class="sxs-lookup"><span data-stu-id="2d127-128">OUTPUTS</span></span>

### <span data-ttu-id="2d127-129">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="2d127-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="2d127-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2d127-130">NOTES</span></span>

## <span data-ttu-id="2d127-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d127-131">RELATED LINKS</span></span>

[<span data-ttu-id="2d127-132">새로운 AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2d127-132">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="2d127-133">제거-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2d127-133">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="2d127-134">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2d127-134">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


