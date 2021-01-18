---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494285"
---
# <span data-ttu-id="c0c1a-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0c1a-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="c0c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c1a-103">Automation 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="c0c1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0c1a-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0c1a-105">설명</span><span class="sxs-lookup"><span data-stu-id="c0c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c1a-106">**New-AzAutomationCredential** cmdlet은 Azure Automation에서 **PSCredential** 개체로 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="c0c1a-107">예제</span><span class="sxs-lookup"><span data-stu-id="c0c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c1a-108">예제 1: 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="c0c1a-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c0c1a-109">첫 번째 명령은 사용자 이름을 $User 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="c0c1a-110">두 번째 명령은 ConvertTo-SecureString cmdlet을 사용하여 일반 텍스트 암호를 보안 문자열로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="c0c1a-111">이 명령은 해당 개체를 $Password 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="c0c1a-112">세 번째 명령은 $User 및 $Password 자격 증명을 만든 다음 $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="c0c1a-113">마지막 명령은 다음을 사용하는 ContosoCredential이라는 Automation 자격 증명을 $Credential.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="c0c1a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0c1a-114">PARAMETERS</span></span>

### <span data-ttu-id="c0c1a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0c1a-115">-AutomationAccountName</span></span>
<span data-ttu-id="c0c1a-116">이 cmdlet이 자격 증명을 저장하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="c0c1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c1a-117">-DefaultProfile</span></span>
<span data-ttu-id="c0c1a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c0c1a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0c1a-119">-Description</span><span class="sxs-lookup"><span data-stu-id="c0c1a-119">-Description</span></span>
<span data-ttu-id="c0c1a-120">자격 증명에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="c0c1a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0c1a-121">-Name</span></span>
<span data-ttu-id="c0c1a-122">자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="c0c1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0c1a-124">이 cmdlet이 자격 증명을 만드는 리소스 그룹에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="c0c1a-125">-Value</span><span class="sxs-lookup"><span data-stu-id="c0c1a-125">-Value</span></span>
<span data-ttu-id="c0c1a-126">자격 증명을 **PSCredential 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="c0c1a-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c1a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c1a-127">CommonParameters</span></span>
<span data-ttu-id="c0c1a-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c1a-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c1a-130">입력</span><span class="sxs-lookup"><span data-stu-id="c0c1a-130">INPUTS</span></span>

### <span data-ttu-id="c0c1a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c0c1a-131">System.String</span></span>

### <span data-ttu-id="c0c1a-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="c0c1a-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="c0c1a-133">출력</span><span class="sxs-lookup"><span data-stu-id="c0c1a-133">OUTPUTS</span></span>

### <span data-ttu-id="c0c1a-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="c0c1a-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="c0c1a-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0c1a-135">NOTES</span></span>

## <span data-ttu-id="c0c1a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0c1a-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0c1a-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0c1a-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="c0c1a-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0c1a-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="c0c1a-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0c1a-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


