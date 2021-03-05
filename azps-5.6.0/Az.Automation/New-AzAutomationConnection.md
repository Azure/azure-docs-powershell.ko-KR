---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: cbd2179501b2df2a0e5f779af764bcdaa0efddc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996949"
---
# <span data-ttu-id="a0797-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a0797-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="a0797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0797-102">SYNOPSIS</span></span>
<span data-ttu-id="a0797-103">Automation 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="a0797-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0797-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0797-105">설명</span><span class="sxs-lookup"><span data-stu-id="a0797-105">DESCRIPTION</span></span>
<span data-ttu-id="a0797-106">**New-AzAutomationConnection** cmdlet은 Azure Automation에서 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="a0797-107">예제</span><span class="sxs-lookup"><span data-stu-id="a0797-107">EXAMPLES</span></span>

### <span data-ttu-id="a0797-108">예제 1: ConnectionTypeName=Azure에 대한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="a0797-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a0797-109">첫 번째 명령은 필드 값의 해시 테이블을 변수에 $FieldValue 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="a0797-110">두 번째 명령은 AutomationAccount01이라는 Automation 계정에 Connection12라는 Azure 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a0797-111">명령은 연결 필드 값을 $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="a0797-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="a0797-112">예제 2: ConnectionTypeName=AzureServicePrincipal에 대한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="a0797-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a0797-113">명령은 AutomationAccount01이라는 Automation 계정에서 Connection13이라는 Azure 연결을 $RunAsAccountConnectionFieldValues ConnectionTypeName=AzureServicePrincipal을 사용하여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="a0797-114">이 ConnectionTypeName=AzureServicePrincipal은 주로 Azure Run As Account에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="a0797-115">예제 3: ConnectionTypeName=AzureClassicCertificate에 대한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="a0797-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a0797-116">명령은 AutomationAccount01이라는 Automation 계정에서 Connection14라는 Azure 연결을 $ClassicRunAsAccountConnectionFieldValues 및 ConnectionTypeName=AzureClassicCertificate를 사용하여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="a0797-117">이 ConnectionTypeName=AzureClassicCertificate는 주로 Azure 클래식 실행 계정으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="a0797-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a0797-118">PARAMETERS</span></span>

### <span data-ttu-id="a0797-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0797-119">-AutomationAccountName</span></span>
<span data-ttu-id="a0797-120">이 cmdlet에서 연결을 만드는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a0797-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="a0797-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="a0797-122">키/값 쌍이 포함된 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="a0797-123">키는 지정된 연결 유형에 대한 연결 필드를 나타내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="a0797-124">값은 연결 인스턴스에 대한 각 연결 필드의 특정 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="a0797-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="a0797-125">-ConnectionTypeName</span></span>
<span data-ttu-id="a0797-126">연결 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="a0797-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0797-127">-DefaultProfile</span></span>
<span data-ttu-id="a0797-128">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0797-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0797-129">-Description</span><span class="sxs-lookup"><span data-stu-id="a0797-129">-Description</span></span>
<span data-ttu-id="a0797-130">연결에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="a0797-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a0797-131">-Name</span></span>
<span data-ttu-id="a0797-132">연결에 대한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="a0797-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0797-133">-ResourceGroupName</span></span>
<span data-ttu-id="a0797-134">이 cmdlet에서 연결을 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a0797-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0797-135">CommonParameters</span></span>
<span data-ttu-id="a0797-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0797-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0797-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a0797-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0797-138">입력</span><span class="sxs-lookup"><span data-stu-id="a0797-138">INPUTS</span></span>

### <span data-ttu-id="a0797-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a0797-139">System.String</span></span>

### <span data-ttu-id="a0797-140">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="a0797-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="a0797-141">출력</span><span class="sxs-lookup"><span data-stu-id="a0797-141">OUTPUTS</span></span>

### <span data-ttu-id="a0797-142">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="a0797-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="a0797-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0797-143">NOTES</span></span>

## <span data-ttu-id="a0797-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0797-144">RELATED LINKS</span></span>

[<span data-ttu-id="a0797-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a0797-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="a0797-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a0797-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


