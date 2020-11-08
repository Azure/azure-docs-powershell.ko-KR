---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056567"
---
# <span data-ttu-id="a8f67-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="a8f67-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="a8f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8f67-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f67-103">자동화 연결의 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="a8f67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8f67-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8f67-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8f67-105">DESCRIPTION</span></span>
<span data-ttu-id="a8f67-106">**Set-AzAutomationConnectionFieldValue** Cmdlet은 Azure Automation의 연결에서 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="a8f67-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a8f67-107">EXAMPLES</span></span>

### <span data-ttu-id="a8f67-108">예제 1: 연결에서 필드 값 변경</span><span class="sxs-lookup"><span data-stu-id="a8f67-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a8f67-109">이 명령은 AutomationAccount01 이라는 Automation 계정에서 ContosoConnection 이라는 Azure 연결에 대 한 구독 ID를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="a8f67-110">변수</span><span class="sxs-lookup"><span data-stu-id="a8f67-110">PARAMETERS</span></span>

### <span data-ttu-id="a8f67-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8f67-111">-AutomationAccountName</span></span>
<span data-ttu-id="a8f67-112">이 cmdlet이 연결의 필드를 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="a8f67-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="a8f67-113">-ConnectionFieldName</span></span>
<span data-ttu-id="a8f67-114">이 cmdlet이 수정 하는 필드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a8f67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f67-115">-DefaultProfile</span></span>
<span data-ttu-id="a8f67-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a8f67-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8f67-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a8f67-117">-Name</span></span>
<span data-ttu-id="a8f67-118">이 cmdlet에서 필드를 수정할 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="a8f67-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f67-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8f67-120">이 cmdlet이 연결의 필드를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="a8f67-121">-값</span><span class="sxs-lookup"><span data-stu-id="a8f67-121">-Value</span></span>
<span data-ttu-id="a8f67-122">연결 필드에서 수정할 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="a8f67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f67-123">CommonParameters</span></span>
<span data-ttu-id="a8f67-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f67-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f67-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f67-126">입력</span><span class="sxs-lookup"><span data-stu-id="a8f67-126">INPUTS</span></span>

### <span data-ttu-id="a8f67-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a8f67-127">System.String</span></span>

### <span data-ttu-id="a8f67-128">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a8f67-128">System.Object</span></span>

## <span data-ttu-id="a8f67-129">출력</span><span class="sxs-lookup"><span data-stu-id="a8f67-129">OUTPUTS</span></span>

### <span data-ttu-id="a8f67-130">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="a8f67-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="a8f67-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a8f67-131">NOTES</span></span>

## <span data-ttu-id="a8f67-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8f67-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8f67-133">새로운 AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a8f67-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


