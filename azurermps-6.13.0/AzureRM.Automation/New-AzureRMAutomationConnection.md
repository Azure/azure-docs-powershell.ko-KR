---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: e86e25cb4752bf6899e1a00fcbccb596b64f8482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529645"
---
# <span data-ttu-id="4aedd-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4aedd-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="4aedd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aedd-102">SYNOPSIS</span></span>
<span data-ttu-id="4aedd-103">자동화 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aedd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4aedd-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aedd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4aedd-105">DESCRIPTION</span></span>
<span data-ttu-id="4aedd-106">**새 AzureRmAutomationConnection** Cmdlet은 Azure Automation에서 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="4aedd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4aedd-107">EXAMPLES</span></span>

### <span data-ttu-id="4aedd-108">예제 1: 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="4aedd-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4aedd-109">첫 번째 명령은 $FieldValue 변수에 필드 값의 해시 테이블을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="4aedd-110">두 번째 명령은 AutomationAccount01 이라는 Automation 계정에 Connection12 이라는 Azure 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="4aedd-111">명령에서 $FieldValues의 연결 필드 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="4aedd-112">변수</span><span class="sxs-lookup"><span data-stu-id="4aedd-112">PARAMETERS</span></span>

### <span data-ttu-id="4aedd-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4aedd-113">-AutomationAccountName</span></span>
<span data-ttu-id="4aedd-114">이 cmdlet이 연결을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4aedd-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="4aedd-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="4aedd-116">키/값 쌍이 포함 된 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="4aedd-117">키는 지정 된 연결 형식에 대 한 연결 필드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="4aedd-118">값은 연결 인스턴스에 대 한 각 연결 필드의 특정 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="4aedd-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4aedd-119">-ConnectionTypeName</span></span>
<span data-ttu-id="4aedd-120">연결 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="4aedd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aedd-121">-DefaultProfile</span></span>
<span data-ttu-id="4aedd-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4aedd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aedd-123">-설명</span><span class="sxs-lookup"><span data-stu-id="4aedd-123">-Description</span></span>
<span data-ttu-id="4aedd-124">연결에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="4aedd-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4aedd-125">-Name</span></span>
<span data-ttu-id="4aedd-126">연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="4aedd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aedd-127">-ResourceGroupName</span></span>
<span data-ttu-id="4aedd-128">이 cmdlet이 연결을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4aedd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aedd-129">CommonParameters</span></span>
<span data-ttu-id="4aedd-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aedd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aedd-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aedd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aedd-132">입력</span><span class="sxs-lookup"><span data-stu-id="4aedd-132">INPUTS</span></span>

### <span data-ttu-id="4aedd-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4aedd-133">System.String</span></span>

### <span data-ttu-id="4aedd-134">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="4aedd-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="4aedd-135">출력</span><span class="sxs-lookup"><span data-stu-id="4aedd-135">OUTPUTS</span></span>

### <span data-ttu-id="4aedd-136">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="4aedd-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="4aedd-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4aedd-137">NOTES</span></span>

## <span data-ttu-id="4aedd-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aedd-138">RELATED LINKS</span></span>

[<span data-ttu-id="4aedd-139">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4aedd-139">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="4aedd-140">제거-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4aedd-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


