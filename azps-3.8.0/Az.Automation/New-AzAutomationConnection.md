---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044973"
---
# <span data-ttu-id="26b51-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="26b51-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="26b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b51-102">SYNOPSIS</span></span>
<span data-ttu-id="26b51-103">자동화 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="26b51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26b51-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26b51-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26b51-105">DESCRIPTION</span></span>
<span data-ttu-id="26b51-106">**새 AzAutomationConnection** Cmdlet은 Azure Automation에서 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="26b51-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26b51-107">EXAMPLES</span></span>

### <span data-ttu-id="26b51-108">예제 1: ConnectionTypeName = Azure에 대 한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="26b51-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="26b51-109">첫 번째 명령은 $FieldValue 변수에 필드 값의 해시 테이블을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="26b51-110">두 번째 명령은 AutomationAccount01 이라는 Automation 계정에 Connection12 이라는 Azure 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="26b51-111">명령에서 $FieldValues의 연결 필드 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="26b51-112">예제 2: ConnectionTypeName = AzureServicePrincipal에 대 한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="26b51-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="26b51-113">이 명령은 $RunAsAccountConnectionFieldValues 및 ConnectionTypeName = AzureServicePrincipal을 사용 하 여 AutomationAccount01 라는 Automation 계정에 Connection13 라는 Azure 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="26b51-114">이 ConnectionTypeName = AzureServicePrincipal은 주로 Azure 실행 계정에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="26b51-115">예제 3: ConnectionTypeName = AzureClassicCertificate에 대 한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="26b51-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="26b51-116">이 명령은 $ClassicRunAsAccountConnectionFieldValues 및 ConnectionTypeName = AzureClassicCertificate를 사용 하 여 AutomationAccount01 이라는 자동화 계정에 Connection14 라는 Azure 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="26b51-117">이 ConnectionTypeName = AzureClassicCertificate은 주로 Azure 클래식 실행 계정에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="26b51-118">변수</span><span class="sxs-lookup"><span data-stu-id="26b51-118">PARAMETERS</span></span>

### <span data-ttu-id="26b51-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="26b51-119">-AutomationAccountName</span></span>
<span data-ttu-id="26b51-120">이 cmdlet이 연결을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="26b51-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="26b51-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="26b51-122">키/값 쌍이 포함 된 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="26b51-123">키는 지정 된 연결 형식에 대 한 연결 필드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="26b51-124">값은 연결 인스턴스에 대 한 각 연결 필드의 특정 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="26b51-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="26b51-125">-ConnectionTypeName</span></span>
<span data-ttu-id="26b51-126">연결 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="26b51-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b51-127">-DefaultProfile</span></span>
<span data-ttu-id="26b51-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26b51-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26b51-129">-설명</span><span class="sxs-lookup"><span data-stu-id="26b51-129">-Description</span></span>
<span data-ttu-id="26b51-130">연결에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="26b51-131">-이름</span><span class="sxs-lookup"><span data-stu-id="26b51-131">-Name</span></span>
<span data-ttu-id="26b51-132">연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="26b51-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b51-133">-ResourceGroupName</span></span>
<span data-ttu-id="26b51-134">이 cmdlet이 연결을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="26b51-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b51-135">CommonParameters</span></span>
<span data-ttu-id="26b51-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b51-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b51-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b51-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b51-138">입력</span><span class="sxs-lookup"><span data-stu-id="26b51-138">INPUTS</span></span>

### <span data-ttu-id="26b51-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26b51-139">System.String</span></span>

### <span data-ttu-id="26b51-140">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="26b51-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="26b51-141">출력</span><span class="sxs-lookup"><span data-stu-id="26b51-141">OUTPUTS</span></span>

### <span data-ttu-id="26b51-142">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="26b51-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="26b51-143">상속자</span><span class="sxs-lookup"><span data-stu-id="26b51-143">NOTES</span></span>

## <span data-ttu-id="26b51-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26b51-144">RELATED LINKS</span></span>

[<span data-ttu-id="26b51-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="26b51-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="26b51-146">제거-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="26b51-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


