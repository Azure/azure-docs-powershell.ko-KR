---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199609"
---
# <span data-ttu-id="0df66-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0df66-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="0df66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df66-102">SYNOPSIS</span></span>
<span data-ttu-id="0df66-103">Automation 자격 증명을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="0df66-104">구문</span><span class="sxs-lookup"><span data-stu-id="0df66-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0df66-105">설명</span><span class="sxs-lookup"><span data-stu-id="0df66-105">DESCRIPTION</span></span>
<span data-ttu-id="0df66-106">**Set-AzAutomationCredential** cmdlet은 Azure Automation에서 **PSCredential** 개체로 자격 증명을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="0df66-107">예제</span><span class="sxs-lookup"><span data-stu-id="0df66-107">EXAMPLES</span></span>

### <span data-ttu-id="0df66-108">예제 1: 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="0df66-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="0df66-109">첫 번째 명령은 사용자 이름을 $User 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="0df66-110">두 번째 명령은 ConvertTo-SecureString cmdlet을 사용하여 일반 텍스트 암호를 보안 문자열로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="0df66-111">이 명령은 해당 개체를 $Password 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="0df66-112">세 번째 명령은 $User 및 $Password 자격 증명을 만든 다음 $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="0df66-113">마지막 명령은 ContosoCredential이라는 Automation 자격 증명을 수정하여 자격 증명을 $Credential.</span><span class="sxs-lookup"><span data-stu-id="0df66-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="0df66-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0df66-114">PARAMETERS</span></span>

### <span data-ttu-id="0df66-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0df66-115">-AutomationAccountName</span></span>
<span data-ttu-id="0df66-116">이 cmdlet이 자격 증명을 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="0df66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df66-117">-DefaultProfile</span></span>
<span data-ttu-id="0df66-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0df66-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0df66-119">-Description</span><span class="sxs-lookup"><span data-stu-id="0df66-119">-Description</span></span>
<span data-ttu-id="0df66-120">이 cmdlet이 수정하는 자격 증명에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0df66-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0df66-121">-Name</span></span>
<span data-ttu-id="0df66-122">이 cmdlet이 수정하는 자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0df66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df66-123">-ResourceGroupName</span></span>
<span data-ttu-id="0df66-124">이 cmdlet이 자격 증명을 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="0df66-125">-Value</span><span class="sxs-lookup"><span data-stu-id="0df66-125">-Value</span></span>
<span data-ttu-id="0df66-126">자격 증명을 **PSCredential 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="0df66-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df66-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df66-127">CommonParameters</span></span>
<span data-ttu-id="0df66-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df66-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0df66-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df66-130">입력</span><span class="sxs-lookup"><span data-stu-id="0df66-130">INPUTS</span></span>

### <span data-ttu-id="0df66-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0df66-131">System.String</span></span>

### <span data-ttu-id="0df66-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="0df66-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="0df66-133">출력</span><span class="sxs-lookup"><span data-stu-id="0df66-133">OUTPUTS</span></span>

### <span data-ttu-id="0df66-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="0df66-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="0df66-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0df66-135">NOTES</span></span>

## <span data-ttu-id="0df66-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0df66-136">RELATED LINKS</span></span>

[<span data-ttu-id="0df66-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0df66-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="0df66-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0df66-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="0df66-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0df66-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


