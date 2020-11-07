---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: fa5faafe9a7d0b7c27e5bb596e56bfadf88e5608
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703480"
---
# <span data-ttu-id="e71b3-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="e71b3-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="e71b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e71b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e71b3-103">자동화 연결의 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e71b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e71b3-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e71b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e71b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e71b3-106">**Set-AzureRmAutomationConnectionFieldValue** Cmdlet은 Azure Automation의 연결에서 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="e71b3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e71b3-107">EXAMPLES</span></span>

### <span data-ttu-id="e71b3-108">예제 1: 연결에서 필드 값 변경</span><span class="sxs-lookup"><span data-stu-id="e71b3-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="e71b3-109">이 명령은 AutomationAccount01 이라는 Automation 계정에서 ContosoConnection 이라는 Azure 연결에 대 한 구독 ID를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="e71b3-110">변수</span><span class="sxs-lookup"><span data-stu-id="e71b3-110">PARAMETERS</span></span>

### <span data-ttu-id="e71b3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e71b3-111">-AutomationAccountName</span></span>
<span data-ttu-id="e71b3-112">이 cmdlet이 연결의 필드를 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="e71b3-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="e71b3-113">-ConnectionFieldName</span></span>
<span data-ttu-id="e71b3-114">이 cmdlet이 수정 하는 필드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e71b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71b3-115">-DefaultProfile</span></span>
<span data-ttu-id="e71b3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e71b3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e71b3-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e71b3-117">-Name</span></span>
<span data-ttu-id="e71b3-118">이 cmdlet에서 필드를 수정할 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="e71b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="e71b3-120">이 cmdlet이 연결의 필드를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="e71b3-121">-값</span><span class="sxs-lookup"><span data-stu-id="e71b3-121">-Value</span></span>
<span data-ttu-id="e71b3-122">연결 필드에서 수정할 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e71b3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71b3-123">CommonParameters</span></span>
<span data-ttu-id="e71b3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71b3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71b3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71b3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71b3-126">입력</span><span class="sxs-lookup"><span data-stu-id="e71b3-126">INPUTS</span></span>

### <span data-ttu-id="e71b3-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e71b3-127">System.String</span></span>

### <span data-ttu-id="e71b3-128">System. 개체</span><span class="sxs-lookup"><span data-stu-id="e71b3-128">System.Object</span></span>

## <span data-ttu-id="e71b3-129">출력</span><span class="sxs-lookup"><span data-stu-id="e71b3-129">OUTPUTS</span></span>

### <span data-ttu-id="e71b3-130">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="e71b3-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="e71b3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e71b3-131">NOTES</span></span>

## <span data-ttu-id="e71b3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e71b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="e71b3-133">새로운 AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e71b3-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


