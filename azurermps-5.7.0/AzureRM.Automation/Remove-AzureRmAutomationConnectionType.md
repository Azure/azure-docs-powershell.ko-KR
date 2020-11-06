---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: c76475a36536e6da68bc7ec5a39790ee96409ea3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525356"
---
# <span data-ttu-id="bb1e1-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="bb1e1-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="bb1e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1e1-103">자동화 연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb1e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb1e1-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb1e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb1e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1e1-106">**AzureRmAutomationConnectionType** Cmdlet은 Azure Automation에서 연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>

<span data-ttu-id="bb1e1-107">삭제 하는 연결 형식과 연결 된 모든 연결을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="bb1e1-108">다음 조건을 충족 하는 새 연결 형식을 만들지 않는 한 해당 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 

- <span data-ttu-id="bb1e1-109">형식의 이름은 원본 연결 형식과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="bb1e1-110">형식에는 원래 연결 형식과 동일한 필드 정의가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="bb1e1-111">추가 필드가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-111">It can have additional fields.</span></span>

## <span data-ttu-id="bb1e1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="bb1e1-112">EXAMPLES</span></span>

### <span data-ttu-id="bb1e1-113">예제 1: 연결 형식 제거</span><span class="sxs-lookup"><span data-stu-id="bb1e1-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bb1e1-114">이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConnectionType 이라는 연결 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bb1e1-115">변수</span><span class="sxs-lookup"><span data-stu-id="bb1e1-115">PARAMETERS</span></span>

### <span data-ttu-id="bb1e1-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb1e1-116">-AutomationAccountName</span></span>
<span data-ttu-id="bb1e1-117">이 cmdlet이 연결 형식을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="bb1e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1e1-118">-DefaultProfile</span></span>
<span data-ttu-id="bb1e1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bb1e1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb1e1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bb1e1-120">-Force</span></span>
<span data-ttu-id="bb1e1-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="bb1e1-121">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1e1-122">-이름</span><span class="sxs-lookup"><span data-stu-id="bb1e1-122">-Name</span></span>
<span data-ttu-id="bb1e1-123">이 cmdlet이 제거 하는 자동화 연결 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb1e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb1e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb1e1-125">이 cmdlet이 자동화 연결 형식을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="bb1e1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="bb1e1-126">-Confirm</span></span>
<span data-ttu-id="bb1e1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1e1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb1e1-128">-WhatIf</span></span>
<span data-ttu-id="bb1e1-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb1e1-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1e1-131">CommonParameters</span></span>
<span data-ttu-id="bb1e1-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1e1-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1e1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1e1-134">입력</span><span class="sxs-lookup"><span data-stu-id="bb1e1-134">INPUTS</span></span>

### <span data-ttu-id="bb1e1-135">않아야</span><span class="sxs-lookup"><span data-stu-id="bb1e1-135">None</span></span>
<span data-ttu-id="bb1e1-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1e1-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb1e1-137">출력</span><span class="sxs-lookup"><span data-stu-id="bb1e1-137">OUTPUTS</span></span>

## <span data-ttu-id="bb1e1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="bb1e1-138">NOTES</span></span>

## <span data-ttu-id="bb1e1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb1e1-139">RELATED LINKS</span></span>

[<span data-ttu-id="bb1e1-140">제거-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bb1e1-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


