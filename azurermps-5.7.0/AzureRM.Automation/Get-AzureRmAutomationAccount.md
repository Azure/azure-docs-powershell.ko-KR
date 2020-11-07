---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711840"
---
# <span data-ttu-id="4b843-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4b843-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="4b843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b843-102">SYNOPSIS</span></span>
<span data-ttu-id="4b843-103">리소스 그룹의 자동화 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b843-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b843-104">SYNTAX</span></span>

### <span data-ttu-id="4b843-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b843-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b843-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b843-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b843-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4b843-107">DESCRIPTION</span></span>
<span data-ttu-id="4b843-108">**Get-AzureRmAutomationAccount** cmdlet은 리소스 그룹의 Azure Automation 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="4b843-109">자동화 계정에 대 한 자세한 내용은 New-AzureRmAutomationAccount cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b843-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="4b843-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4b843-110">EXAMPLES</span></span>

### <span data-ttu-id="4b843-111">예제 1: 모든 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="4b843-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="4b843-112">이 명령은 ResourceGroup03 이라는 리소스 그룹의 모든 자동화 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="4b843-113">예제 2: 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="4b843-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="4b843-114">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 ContosoAutomationAccount 라는 Automation 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="4b843-115">변수</span><span class="sxs-lookup"><span data-stu-id="4b843-115">PARAMETERS</span></span>

### <span data-ttu-id="4b843-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b843-116">-DefaultProfile</span></span>
<span data-ttu-id="4b843-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b843-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b843-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4b843-118">-Name</span></span>
<span data-ttu-id="4b843-119">이 cmdlet이 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b843-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b843-120">-ResourceGroupName</span></span>
<span data-ttu-id="4b843-121">이 cmdlet에서 자동화 계정을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b843-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b843-122">CommonParameters</span></span>
<span data-ttu-id="4b843-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b843-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b843-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b843-125">입력</span><span class="sxs-lookup"><span data-stu-id="4b843-125">INPUTS</span></span>

### <span data-ttu-id="4b843-126">않아야</span><span class="sxs-lookup"><span data-stu-id="4b843-126">None</span></span>
<span data-ttu-id="4b843-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b843-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b843-128">출력</span><span class="sxs-lookup"><span data-stu-id="4b843-128">OUTPUTS</span></span>

### <span data-ttu-id="4b843-129">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="4b843-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="4b843-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4b843-130">NOTES</span></span>

## <span data-ttu-id="4b843-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b843-131">RELATED LINKS</span></span>

[<span data-ttu-id="4b843-132">새로운 AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4b843-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="4b843-133">제거-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4b843-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="4b843-134">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4b843-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


