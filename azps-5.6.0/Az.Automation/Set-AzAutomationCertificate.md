---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 80a33fe4664e4c7814db6774e7cd427dd9a2c87e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957728"
---
# <span data-ttu-id="bc5fc-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc5fc-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="bc5fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5fc-103">Automation 인증서의 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="bc5fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc5fc-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc5fc-105">설명</span><span class="sxs-lookup"><span data-stu-id="bc5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5fc-106">**Set-AzAutomationCertificate** cmdlet은 Azure Automation에서 인증서 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="bc5fc-107">예제</span><span class="sxs-lookup"><span data-stu-id="bc5fc-107">EXAMPLES</span></span>

### <span data-ttu-id="bc5fc-108">예제 1: 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="bc5fc-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bc5fc-109">첫 번째 명령은 일반 텍스트 암호를 cmdlet을 사용하여 보안 문자열로 ConvertTo-SecureString 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="bc5fc-110">명령은 해당 개체를 $Password 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="bc5fc-111">두 번째 명령은 ContosoCertificate라는 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="bc5fc-112">명령은 에 저장된 암호를 $Password.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="bc5fc-113">명령은 업로드하는 파일의 계정 이름과 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="bc5fc-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bc5fc-114">PARAMETERS</span></span>

### <span data-ttu-id="bc5fc-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc5fc-115">-AutomationAccountName</span></span>
<span data-ttu-id="bc5fc-116">이 cmdlet에서 인증서를 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="bc5fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5fc-117">-DefaultProfile</span></span>
<span data-ttu-id="bc5fc-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bc5fc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc5fc-119">-Description</span><span class="sxs-lookup"><span data-stu-id="bc5fc-119">-Description</span></span>
<span data-ttu-id="bc5fc-120">이 cmdlet이 수정하는 인증서에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bc5fc-121">-내보내기 가능</span><span class="sxs-lookup"><span data-stu-id="bc5fc-121">-Exportable</span></span>
<span data-ttu-id="bc5fc-122">인증서를 내보낼 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bc5fc-123">-Name</span></span>
<span data-ttu-id="bc5fc-124">이 cmdlet이 수정하는 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bc5fc-125">-Password</span><span class="sxs-lookup"><span data-stu-id="bc5fc-125">-Password</span></span>
<span data-ttu-id="bc5fc-126">인증서 파일의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fc-127">-Path</span><span class="sxs-lookup"><span data-stu-id="bc5fc-127">-Path</span></span>
<span data-ttu-id="bc5fc-128">업로드할 스크립트 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="bc5fc-129">파일은 .cer 파일 또는 .pfx 파일일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="bc5fc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc5fc-130">-ResourceGroupName</span></span>
<span data-ttu-id="bc5fc-131">이 cmdlet에서 인증서를 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="bc5fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5fc-132">CommonParameters</span></span>
<span data-ttu-id="bc5fc-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5fc-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5fc-135">입력</span><span class="sxs-lookup"><span data-stu-id="bc5fc-135">INPUTS</span></span>

### <span data-ttu-id="bc5fc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bc5fc-136">System.String</span></span>

### <span data-ttu-id="bc5fc-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="bc5fc-137">System.Security.SecureString</span></span>

### <span data-ttu-id="bc5fc-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc5fc-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bc5fc-139">출력</span><span class="sxs-lookup"><span data-stu-id="bc5fc-139">OUTPUTS</span></span>

### <span data-ttu-id="bc5fc-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="bc5fc-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="bc5fc-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc5fc-141">NOTES</span></span>

## <span data-ttu-id="bc5fc-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc5fc-142">RELATED LINKS</span></span>

[<span data-ttu-id="bc5fc-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc5fc-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="bc5fc-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc5fc-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="bc5fc-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc5fc-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


