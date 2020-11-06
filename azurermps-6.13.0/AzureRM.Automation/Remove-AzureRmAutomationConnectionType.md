---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 9598280ecae0ce8aca94fd16ae40928dba7a2404
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528665"
---
# <span data-ttu-id="5867d-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="5867d-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="5867d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5867d-102">SYNOPSIS</span></span>
<span data-ttu-id="5867d-103">자동화 연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5867d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5867d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5867d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5867d-105">DESCRIPTION</span></span>
<span data-ttu-id="5867d-106">**AzureRmAutomationConnectionType** Cmdlet은 Azure Automation에서 연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="5867d-107">삭제 하는 연결 형식과 연결 된 모든 연결을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="5867d-108">다음 조건을 충족 하는 새 연결 형식을 만들지 않는 한 해당 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="5867d-109">형식의 이름은 원본 연결 형식과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="5867d-110">형식에는 원래 연결 형식과 동일한 필드 정의가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="5867d-111">추가 필드가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-111">It can have additional fields.</span></span>

## <span data-ttu-id="5867d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5867d-112">EXAMPLES</span></span>

### <span data-ttu-id="5867d-113">예제 1: 연결 형식 제거</span><span class="sxs-lookup"><span data-stu-id="5867d-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5867d-114">이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConnectionType 이라는 연결 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5867d-115">변수</span><span class="sxs-lookup"><span data-stu-id="5867d-115">PARAMETERS</span></span>

### <span data-ttu-id="5867d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5867d-116">-AutomationAccountName</span></span>
<span data-ttu-id="5867d-117">이 cmdlet이 연결 형식을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="5867d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5867d-118">-DefaultProfile</span></span>
<span data-ttu-id="5867d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5867d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5867d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5867d-120">-Force</span></span>
<span data-ttu-id="5867d-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="5867d-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5867d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="5867d-122">-Name</span></span>
<span data-ttu-id="5867d-123">이 cmdlet이 제거 하는 자동화 연결 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5867d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5867d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5867d-125">이 cmdlet이 자동화 연결 형식을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="5867d-126">-확인</span><span class="sxs-lookup"><span data-stu-id="5867d-126">-Confirm</span></span>
<span data-ttu-id="5867d-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5867d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5867d-128">-WhatIf</span></span>
<span data-ttu-id="5867d-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5867d-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5867d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5867d-131">CommonParameters</span></span>
<span data-ttu-id="5867d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5867d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5867d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5867d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5867d-134">입력</span><span class="sxs-lookup"><span data-stu-id="5867d-134">INPUTS</span></span>

### <span data-ttu-id="5867d-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5867d-135">System.String</span></span>

## <span data-ttu-id="5867d-136">출력</span><span class="sxs-lookup"><span data-stu-id="5867d-136">OUTPUTS</span></span>

### <span data-ttu-id="5867d-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="5867d-137">System.Void</span></span>

## <span data-ttu-id="5867d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="5867d-138">NOTES</span></span>

## <span data-ttu-id="5867d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5867d-139">RELATED LINKS</span></span>

[<span data-ttu-id="5867d-140">제거-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5867d-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


