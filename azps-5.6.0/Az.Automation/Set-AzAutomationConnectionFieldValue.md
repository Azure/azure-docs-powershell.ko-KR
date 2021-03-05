---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: d11b99352d3a3f75c24e47cabfe06e816958fb82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004736"
---
# <span data-ttu-id="071d8-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="071d8-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="071d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="071d8-102">SYNOPSIS</span></span>
<span data-ttu-id="071d8-103">Automation 연결에서 필드 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="071d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="071d8-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="071d8-105">설명</span><span class="sxs-lookup"><span data-stu-id="071d8-105">DESCRIPTION</span></span>
<span data-ttu-id="071d8-106">**Set-AzAutomationConnectionFieldValue** cmdlet은 Azure Automation의 연결에서 필드 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="071d8-107">예제</span><span class="sxs-lookup"><span data-stu-id="071d8-107">EXAMPLES</span></span>

### <span data-ttu-id="071d8-108">예제 1: 연결에서 필드 값 변경</span><span class="sxs-lookup"><span data-stu-id="071d8-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="071d8-109">이 명령은 AutomationAccount01이라는 Automation 계정에서 ContosoConnection이라는 Azure 연결에 대한 구독 ID를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="071d8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="071d8-110">PARAMETERS</span></span>

### <span data-ttu-id="071d8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="071d8-111">-AutomationAccountName</span></span>
<span data-ttu-id="071d8-112">이 cmdlet이 연결의 필드를 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="071d8-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="071d8-113">-ConnectionFieldName</span></span>
<span data-ttu-id="071d8-114">이 cmdlet이 수정하는 필드의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="071d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="071d8-115">-DefaultProfile</span></span>
<span data-ttu-id="071d8-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="071d8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="071d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="071d8-117">-Name</span></span>
<span data-ttu-id="071d8-118">이 cmdlet이 필드를 수정하는 연결의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="071d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="071d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="071d8-120">이 cmdlet이 연결의 필드를 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="071d8-121">-Value</span><span class="sxs-lookup"><span data-stu-id="071d8-121">-Value</span></span>
<span data-ttu-id="071d8-122">연결 필드에서 수정할 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="071d8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071d8-123">CommonParameters</span></span>
<span data-ttu-id="071d8-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="071d8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071d8-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="071d8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071d8-126">입력</span><span class="sxs-lookup"><span data-stu-id="071d8-126">INPUTS</span></span>

### <span data-ttu-id="071d8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="071d8-127">System.String</span></span>

### <span data-ttu-id="071d8-128">System.Object</span><span class="sxs-lookup"><span data-stu-id="071d8-128">System.Object</span></span>

## <span data-ttu-id="071d8-129">출력</span><span class="sxs-lookup"><span data-stu-id="071d8-129">OUTPUTS</span></span>

### <span data-ttu-id="071d8-130">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="071d8-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="071d8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="071d8-131">NOTES</span></span>

## <span data-ttu-id="071d8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="071d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="071d8-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="071d8-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


