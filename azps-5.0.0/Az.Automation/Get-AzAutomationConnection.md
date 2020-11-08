---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216137"
---
# <span data-ttu-id="51801-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="51801-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="51801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51801-102">SYNOPSIS</span></span>
<span data-ttu-id="51801-103">자동화 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51801-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="51801-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51801-104">SYNTAX</span></span>

### <span data-ttu-id="51801-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="51801-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51801-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="51801-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51801-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="51801-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51801-108">설명은</span><span class="sxs-lookup"><span data-stu-id="51801-108">DESCRIPTION</span></span>
<span data-ttu-id="51801-109">**AzAutomationConnection** cmdlet은 하나 이상의 Azure 자동화 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51801-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="51801-110">기본적으로이 cmdlet은 모든 연결을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="51801-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="51801-111">특정 연결을 얻으려면 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51801-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="51801-112">연결 형식 이름을 지정 하 여 특정 유형의 모든 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51801-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="51801-113">예제의</span><span class="sxs-lookup"><span data-stu-id="51801-113">EXAMPLES</span></span>

### <span data-ttu-id="51801-114">예제 1: 모든 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="51801-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="51801-115">이 명령은 Contoso17 이라는 Automation 계정의 모든 연결에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51801-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="51801-116">예제 2: 형식의 모든 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="51801-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="51801-117">이 명령은 Contoso17 이라는 Automation 계정의 연결에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51801-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="51801-118">이 명령은 SqlServer 형식에 대 한 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51801-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="51801-119">예제 3: 연결 하기</span><span class="sxs-lookup"><span data-stu-id="51801-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="51801-120">이 명령은 ContosoConnection 이라는 연결에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51801-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="51801-121">변수</span><span class="sxs-lookup"><span data-stu-id="51801-121">PARAMETERS</span></span>

### <span data-ttu-id="51801-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="51801-122">-AutomationAccountName</span></span>
<span data-ttu-id="51801-123">이 cmdlet이 연결을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51801-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="51801-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="51801-124">-ConnectionTypeName</span></span>
<span data-ttu-id="51801-125">이 cmdlet이 연결을 검색 하는 연결 유형의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51801-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="51801-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51801-126">-DefaultProfile</span></span>
<span data-ttu-id="51801-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="51801-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51801-128">-이름</span><span class="sxs-lookup"><span data-stu-id="51801-128">-Name</span></span>
<span data-ttu-id="51801-129">이 cmdlet에서 검색 하는 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51801-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="51801-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51801-130">-ResourceGroupName</span></span>
<span data-ttu-id="51801-131">이 cmdlet이 연결을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51801-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="51801-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51801-132">CommonParameters</span></span>
<span data-ttu-id="51801-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51801-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51801-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51801-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51801-135">입력</span><span class="sxs-lookup"><span data-stu-id="51801-135">INPUTS</span></span>

### <span data-ttu-id="51801-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="51801-136">System.String</span></span>

## <span data-ttu-id="51801-137">출력</span><span class="sxs-lookup"><span data-stu-id="51801-137">OUTPUTS</span></span>

### <span data-ttu-id="51801-138">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="51801-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="51801-139">상속자</span><span class="sxs-lookup"><span data-stu-id="51801-139">NOTES</span></span>

## <span data-ttu-id="51801-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51801-140">RELATED LINKS</span></span>

[<span data-ttu-id="51801-141">새로운 AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="51801-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="51801-142">제거-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="51801-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


