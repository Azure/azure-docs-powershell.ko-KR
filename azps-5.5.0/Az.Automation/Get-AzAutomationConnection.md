---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201225"
---
# <span data-ttu-id="4b634-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4b634-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="4b634-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b634-102">SYNOPSIS</span></span>
<span data-ttu-id="4b634-103">Automation 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="4b634-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b634-104">SYNTAX</span></span>

### <span data-ttu-id="4b634-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b634-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b634-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="4b634-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b634-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4b634-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b634-108">설명</span><span class="sxs-lookup"><span data-stu-id="4b634-108">DESCRIPTION</span></span>
<span data-ttu-id="4b634-109">**Get-AzAutomationConnection** cmdlet은 하나 이상의 Azure Automation 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="4b634-110">기본적으로 이 cmdlet은 모든 연결을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="4b634-111">특정 연결을 얻을 연결의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="4b634-112">특정 형식의 모든 연결을 얻게 하는 연결 형식 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="4b634-113">예제</span><span class="sxs-lookup"><span data-stu-id="4b634-113">EXAMPLES</span></span>

### <span data-ttu-id="4b634-114">예제 1: 모든 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="4b634-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4b634-115">이 명령은 Contoso17이라는 Automation 계정의 모든 연결에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4b634-116">예제 2: 형식의 모든 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="4b634-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="4b634-117">이 명령은 Contoso17이라는 Automation 계정의 연결에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4b634-118">이 명령은 SqlServer 형식의 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="4b634-119">예제 3: 연결하기</span><span class="sxs-lookup"><span data-stu-id="4b634-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="4b634-120">이 명령은 ContosoConnection이라는 연결에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="4b634-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b634-121">PARAMETERS</span></span>

### <span data-ttu-id="4b634-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b634-122">-AutomationAccountName</span></span>
<span data-ttu-id="4b634-123">이 cmdlet에서 연결을 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="4b634-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4b634-124">-ConnectionTypeName</span></span>
<span data-ttu-id="4b634-125">이 cmdlet이 연결을 검색하는 연결 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b634-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b634-126">-DefaultProfile</span></span>
<span data-ttu-id="4b634-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b634-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b634-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4b634-128">-Name</span></span>
<span data-ttu-id="4b634-129">이 cmdlet이 검색하는 연결의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b634-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b634-130">-ResourceGroupName</span></span>
<span data-ttu-id="4b634-131">이 cmdlet에서 연결을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="4b634-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b634-132">CommonParameters</span></span>
<span data-ttu-id="4b634-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b634-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b634-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4b634-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b634-135">입력</span><span class="sxs-lookup"><span data-stu-id="4b634-135">INPUTS</span></span>

### <span data-ttu-id="4b634-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4b634-136">System.String</span></span>

## <span data-ttu-id="4b634-137">출력</span><span class="sxs-lookup"><span data-stu-id="4b634-137">OUTPUTS</span></span>

### <span data-ttu-id="4b634-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="4b634-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="4b634-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b634-139">NOTES</span></span>

## <span data-ttu-id="4b634-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b634-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b634-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4b634-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="4b634-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4b634-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


