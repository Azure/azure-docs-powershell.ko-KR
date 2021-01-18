---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494349"
---
# <span data-ttu-id="bf5a0-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf5a0-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="bf5a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf5a0-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5a0-103">Automation 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="bf5a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf5a0-104">SYNTAX</span></span>

### <span data-ttu-id="bf5a0-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="bf5a0-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf5a0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bf5a0-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf5a0-107">설명</span><span class="sxs-lookup"><span data-stu-id="bf5a0-107">DESCRIPTION</span></span>
<span data-ttu-id="bf5a0-108">**Get-AzAutomationCredential** cmdlet은 하나 이상의 Azure Automation 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="bf5a0-109">기본적으로 모든 자격 증명이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="bf5a0-110">특정 자격 증명을 얻을 자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="bf5a0-111">보안을 위해 이 cmdlet은 자격 증명 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="bf5a0-112">예제</span><span class="sxs-lookup"><span data-stu-id="bf5a0-112">EXAMPLES</span></span>

### <span data-ttu-id="bf5a0-113">예제 1: 모든 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="bf5a0-114">이 명령은 Contoso17이라는 Automation 계정의 모든 자격 증명에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bf5a0-115">예제 2: 자격 증명 얻기</span><span class="sxs-lookup"><span data-stu-id="bf5a0-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="bf5a0-116">이 명령은 Contoso17이라는 Automation 계정에서 ContosoCredential이라는 자격 증명에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bf5a0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf5a0-117">PARAMETERS</span></span>

### <span data-ttu-id="bf5a0-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bf5a0-118">-AutomationAccountName</span></span>
<span data-ttu-id="bf5a0-119">이 cmdlet이 자격 증명을 검색하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="bf5a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5a0-120">-DefaultProfile</span></span>
<span data-ttu-id="bf5a0-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bf5a0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf5a0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bf5a0-122">-Name</span></span>
<span data-ttu-id="bf5a0-123">검색할 자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf5a0-125">이 cmdlet이 자격 증명을 검색하는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="bf5a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5a0-126">CommonParameters</span></span>
<span data-ttu-id="bf5a0-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5a0-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bf5a0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5a0-129">입력</span><span class="sxs-lookup"><span data-stu-id="bf5a0-129">INPUTS</span></span>

### <span data-ttu-id="bf5a0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bf5a0-130">System.String</span></span>

## <span data-ttu-id="bf5a0-131">출력</span><span class="sxs-lookup"><span data-stu-id="bf5a0-131">OUTPUTS</span></span>

### <span data-ttu-id="bf5a0-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="bf5a0-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="bf5a0-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf5a0-133">NOTES</span></span>

## <span data-ttu-id="bf5a0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf5a0-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf5a0-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf5a0-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="bf5a0-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf5a0-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="bf5a0-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf5a0-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


