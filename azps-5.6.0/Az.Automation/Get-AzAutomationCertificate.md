---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 1680f4080f0e3def2e18d90273ce9e6f2f6d0bcb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993076"
---
# <span data-ttu-id="ba617-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba617-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="ba617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba617-102">SYNOPSIS</span></span>
<span data-ttu-id="ba617-103">Automation 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="ba617-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba617-104">SYNTAX</span></span>

### <span data-ttu-id="ba617-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="ba617-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba617-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="ba617-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba617-107">설명</span><span class="sxs-lookup"><span data-stu-id="ba617-107">DESCRIPTION</span></span>
<span data-ttu-id="ba617-108">**Get-AzAutomationCertificate** cmdlet은 하나 이상의 Azure Automation 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="ba617-109">기본적으로 이 cmdlet은 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="ba617-110">특정 인증서를 얻을 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="ba617-111">예제</span><span class="sxs-lookup"><span data-stu-id="ba617-111">EXAMPLES</span></span>

### <span data-ttu-id="ba617-112">예제 1: 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="ba617-113">이 명령은 Contoso17이라는 Automation 계정의 모든 인증서에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="ba617-114">예제 2: 인증서를 얻다</span><span class="sxs-lookup"><span data-stu-id="ba617-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="ba617-115">이 명령은 ContosoCertificate라는 인증서에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="ba617-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ba617-116">PARAMETERS</span></span>

### <span data-ttu-id="ba617-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba617-117">-AutomationAccountName</span></span>
<span data-ttu-id="ba617-118">이 cmdlet이 인증서를 검색하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="ba617-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba617-119">-DefaultProfile</span></span>
<span data-ttu-id="ba617-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ba617-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba617-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ba617-121">-Name</span></span>
<span data-ttu-id="ba617-122">검색할 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba617-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba617-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba617-124">이 cmdlet에서 Automation 인증서를 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="ba617-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba617-125">CommonParameters</span></span>
<span data-ttu-id="ba617-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba617-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba617-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ba617-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba617-128">입력</span><span class="sxs-lookup"><span data-stu-id="ba617-128">INPUTS</span></span>

### <span data-ttu-id="ba617-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ba617-129">System.String</span></span>

## <span data-ttu-id="ba617-130">출력</span><span class="sxs-lookup"><span data-stu-id="ba617-130">OUTPUTS</span></span>

### <span data-ttu-id="ba617-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="ba617-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ba617-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba617-132">NOTES</span></span>

## <span data-ttu-id="ba617-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba617-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba617-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba617-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="ba617-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba617-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="ba617-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba617-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


