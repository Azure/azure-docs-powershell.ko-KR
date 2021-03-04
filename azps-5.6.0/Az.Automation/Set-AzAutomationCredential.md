---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 6fbef2bcedf4de93cd816f6a4702ee01df10d17f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957723"
---
# <span data-ttu-id="d0d53-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d0d53-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="d0d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0d53-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d53-103">Automation 자격 증명을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="d0d53-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0d53-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0d53-105">설명</span><span class="sxs-lookup"><span data-stu-id="d0d53-105">DESCRIPTION</span></span>
<span data-ttu-id="d0d53-106">**Set-AzAutomationCredential** cmdlet은 Azure Automation에서 **PSCredential** 개체로 자격 증명을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="d0d53-107">예제</span><span class="sxs-lookup"><span data-stu-id="d0d53-107">EXAMPLES</span></span>

### <span data-ttu-id="d0d53-108">예제 1: 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="d0d53-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="d0d53-109">첫 번째 명령은 사용자 이름을 $User 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="d0d53-110">두 번째 명령은 ConvertTo-SecureString cmdlet을 사용하여 일반 텍스트 암호를 보안 문자열로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="d0d53-111">명령은 해당 개체를 $Password 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="d0d53-112">세 번째 명령은 $User 및 $Password 따라 자격 증명을 만든 다음 $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="d0d53-113">마지막 명령은 ContosoCredential이라는 Automation 자격 증명을 수정하여 자격 증명을 $Credential.</span><span class="sxs-lookup"><span data-stu-id="d0d53-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="d0d53-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0d53-114">PARAMETERS</span></span>

### <span data-ttu-id="d0d53-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0d53-115">-AutomationAccountName</span></span>
<span data-ttu-id="d0d53-116">이 cmdlet에서 자격 증명을 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="d0d53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d53-117">-DefaultProfile</span></span>
<span data-ttu-id="d0d53-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d0d53-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0d53-119">-Description</span><span class="sxs-lookup"><span data-stu-id="d0d53-119">-Description</span></span>
<span data-ttu-id="d0d53-120">이 cmdlet이 수정하는 자격 증명에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d0d53-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d0d53-121">-Name</span></span>
<span data-ttu-id="d0d53-122">이 cmdlet이 수정하는 자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d0d53-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0d53-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0d53-124">이 cmdlet에서 자격 증명을 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="d0d53-125">-Value</span><span class="sxs-lookup"><span data-stu-id="d0d53-125">-Value</span></span>
<span data-ttu-id="d0d53-126">자격 증명을 **PSCredential 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="d0d53-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="d0d53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d53-127">CommonParameters</span></span>
<span data-ttu-id="d0d53-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d53-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d0d53-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d53-130">입력</span><span class="sxs-lookup"><span data-stu-id="d0d53-130">INPUTS</span></span>

### <span data-ttu-id="d0d53-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d0d53-131">System.String</span></span>

### <span data-ttu-id="d0d53-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="d0d53-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="d0d53-133">출력</span><span class="sxs-lookup"><span data-stu-id="d0d53-133">OUTPUTS</span></span>

### <span data-ttu-id="d0d53-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="d0d53-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="d0d53-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0d53-135">NOTES</span></span>

## <span data-ttu-id="d0d53-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0d53-136">RELATED LINKS</span></span>

[<span data-ttu-id="d0d53-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d0d53-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="d0d53-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d0d53-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="d0d53-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d0d53-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


