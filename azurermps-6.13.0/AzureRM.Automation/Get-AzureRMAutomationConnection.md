---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: 6397c1efdce39e575caa98558a54bd279fd0374e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534516"
---
# <span data-ttu-id="3556d-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3556d-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="3556d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3556d-102">SYNOPSIS</span></span>
<span data-ttu-id="3556d-103">자동화 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3556d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3556d-104">SYNTAX</span></span>

### <span data-ttu-id="3556d-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="3556d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3556d-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="3556d-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3556d-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="3556d-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3556d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3556d-108">DESCRIPTION</span></span>
<span data-ttu-id="3556d-109">**AzureRmAutomationConnection** cmdlet은 하나 이상의 Azure 자동화 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="3556d-110">기본적으로이 cmdlet은 모든 연결을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="3556d-111">특정 연결을 얻으려면 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="3556d-112">연결 형식 이름을 지정 하 여 특정 유형의 모든 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="3556d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="3556d-113">EXAMPLES</span></span>

### <span data-ttu-id="3556d-114">예제 1: 모든 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="3556d-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3556d-115">이 명령은 Contoso17 이라는 Automation 계정의 모든 연결에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3556d-116">예제 2: 형식의 모든 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="3556d-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="3556d-117">이 명령은 Contoso17 이라는 Automation 계정의 연결에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="3556d-118">이 명령은 SqlServer 형식에 대 한 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="3556d-119">예제 3: 연결 하기</span><span class="sxs-lookup"><span data-stu-id="3556d-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="3556d-120">이 명령은 ContosoConnection 이라는 연결에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="3556d-121">변수</span><span class="sxs-lookup"><span data-stu-id="3556d-121">PARAMETERS</span></span>

### <span data-ttu-id="3556d-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3556d-122">-AutomationAccountName</span></span>
<span data-ttu-id="3556d-123">이 cmdlet이 연결을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="3556d-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="3556d-124">-ConnectionTypeName</span></span>
<span data-ttu-id="3556d-125">이 cmdlet이 연결을 검색 하는 연결 유형의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="3556d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3556d-126">-DefaultProfile</span></span>
<span data-ttu-id="3556d-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3556d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3556d-128">-이름</span><span class="sxs-lookup"><span data-stu-id="3556d-128">-Name</span></span>
<span data-ttu-id="3556d-129">이 cmdlet에서 검색 하는 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="3556d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3556d-130">-ResourceGroupName</span></span>
<span data-ttu-id="3556d-131">이 cmdlet이 연결을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="3556d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3556d-132">CommonParameters</span></span>
<span data-ttu-id="3556d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3556d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3556d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3556d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3556d-135">입력</span><span class="sxs-lookup"><span data-stu-id="3556d-135">INPUTS</span></span>

### <span data-ttu-id="3556d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3556d-136">System.String</span></span>

## <span data-ttu-id="3556d-137">출력</span><span class="sxs-lookup"><span data-stu-id="3556d-137">OUTPUTS</span></span>

### <span data-ttu-id="3556d-138">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="3556d-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="3556d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="3556d-139">NOTES</span></span>

## <span data-ttu-id="3556d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3556d-140">RELATED LINKS</span></span>

[<span data-ttu-id="3556d-141">새로운 AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3556d-141">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="3556d-142">제거-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3556d-142">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


