---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: 84da08588838982353bc8c39354452bec1a17a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533787"
---
# <span data-ttu-id="781fb-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="781fb-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="781fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="781fb-102">SYNOPSIS</span></span>
<span data-ttu-id="781fb-103">자동화 연결의 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="781fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="781fb-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="781fb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="781fb-105">DESCRIPTION</span></span>
<span data-ttu-id="781fb-106">**Set-AzureRmAutomationConnectionFieldValue** Cmdlet은 Azure Automation의 연결에서 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="781fb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="781fb-107">EXAMPLES</span></span>

### <span data-ttu-id="781fb-108">예제 1: 연결에서 필드 값 변경</span><span class="sxs-lookup"><span data-stu-id="781fb-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="781fb-109">이 명령은 AutomationAccount01 이라는 Automation 계정에서 ContosoConnection 이라는 Azure 연결에 대 한 구독 ID를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="781fb-110">변수</span><span class="sxs-lookup"><span data-stu-id="781fb-110">PARAMETERS</span></span>

### <span data-ttu-id="781fb-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="781fb-111">-AutomationAccountName</span></span>
<span data-ttu-id="781fb-112">이 cmdlet이 연결의 필드를 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="781fb-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="781fb-113">-ConnectionFieldName</span></span>
<span data-ttu-id="781fb-114">이 cmdlet이 수정 하는 필드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="781fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781fb-115">-DefaultProfile</span></span>
<span data-ttu-id="781fb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="781fb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="781fb-117">-이름</span><span class="sxs-lookup"><span data-stu-id="781fb-117">-Name</span></span>
<span data-ttu-id="781fb-118">이 cmdlet에서 필드를 수정할 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="781fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="781fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="781fb-120">이 cmdlet이 연결의 필드를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="781fb-121">-값</span><span class="sxs-lookup"><span data-stu-id="781fb-121">-Value</span></span>
<span data-ttu-id="781fb-122">연결 필드에서 수정할 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="781fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781fb-123">CommonParameters</span></span>
<span data-ttu-id="781fb-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781fb-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="781fb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781fb-126">입력</span><span class="sxs-lookup"><span data-stu-id="781fb-126">INPUTS</span></span>

### <span data-ttu-id="781fb-127">않아야</span><span class="sxs-lookup"><span data-stu-id="781fb-127">None</span></span>
<span data-ttu-id="781fb-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="781fb-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="781fb-129">출력</span><span class="sxs-lookup"><span data-stu-id="781fb-129">OUTPUTS</span></span>

### <span data-ttu-id="781fb-130">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="781fb-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="781fb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="781fb-131">NOTES</span></span>

## <span data-ttu-id="781fb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="781fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="781fb-133">새로운 AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="781fb-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


