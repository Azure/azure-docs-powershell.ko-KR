---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701573"
---
# <span data-ttu-id="73fef-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="73fef-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="73fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73fef-102">SYNOPSIS</span></span>
<span data-ttu-id="73fef-103">자동화 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="73fef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73fef-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73fef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73fef-105">DESCRIPTION</span></span>
<span data-ttu-id="73fef-106">**새 AzAutomationConnection** Cmdlet은 Azure Automation에서 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="73fef-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73fef-107">EXAMPLES</span></span>

### <span data-ttu-id="73fef-108">예제 1: 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="73fef-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="73fef-109">첫 번째 명령은 $FieldValue 변수에 필드 값의 해시 테이블을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="73fef-110">두 번째 명령은 AutomationAccount01 이라는 Automation 계정에 Connection12 이라는 Azure 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="73fef-111">명령에서 $FieldValues의 연결 필드 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="73fef-112">변수</span><span class="sxs-lookup"><span data-stu-id="73fef-112">PARAMETERS</span></span>

### <span data-ttu-id="73fef-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="73fef-113">-AutomationAccountName</span></span>
<span data-ttu-id="73fef-114">이 cmdlet이 연결을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="73fef-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="73fef-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="73fef-116">키/값 쌍이 포함 된 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="73fef-117">키는 지정 된 연결 형식에 대 한 연결 필드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="73fef-118">값은 연결 인스턴스에 대 한 각 연결 필드의 특정 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fef-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="73fef-119">-ConnectionTypeName</span></span>
<span data-ttu-id="73fef-120">연결 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-120">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fef-121">-DefaultProfile</span></span>
<span data-ttu-id="73fef-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="73fef-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73fef-123">-설명</span><span class="sxs-lookup"><span data-stu-id="73fef-123">-Description</span></span>
<span data-ttu-id="73fef-124">연결에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-124">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fef-125">-이름</span><span class="sxs-lookup"><span data-stu-id="73fef-125">-Name</span></span>
<span data-ttu-id="73fef-126">연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="73fef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73fef-127">-ResourceGroupName</span></span>
<span data-ttu-id="73fef-128">이 cmdlet이 연결을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="73fef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fef-129">CommonParameters</span></span>
<span data-ttu-id="73fef-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fef-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73fef-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fef-132">입력</span><span class="sxs-lookup"><span data-stu-id="73fef-132">INPUTS</span></span>

### <span data-ttu-id="73fef-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73fef-133">System.String</span></span>

### <span data-ttu-id="73fef-134">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="73fef-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="73fef-135">출력</span><span class="sxs-lookup"><span data-stu-id="73fef-135">OUTPUTS</span></span>

### <span data-ttu-id="73fef-136">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="73fef-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="73fef-137">상속자</span><span class="sxs-lookup"><span data-stu-id="73fef-137">NOTES</span></span>

## <span data-ttu-id="73fef-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73fef-138">RELATED LINKS</span></span>

[<span data-ttu-id="73fef-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="73fef-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="73fef-140">제거-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="73fef-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


