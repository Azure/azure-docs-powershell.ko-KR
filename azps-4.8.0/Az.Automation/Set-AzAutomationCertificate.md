---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212633"
---
# <span data-ttu-id="667fd-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="667fd-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="667fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667fd-102">SYNOPSIS</span></span>
<span data-ttu-id="667fd-103">자동화 인증서의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="667fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="667fd-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="667fd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="667fd-105">DESCRIPTION</span></span>
<span data-ttu-id="667fd-106">**AzAutomationCertificate** Cmdlet은 Azure Automation에서 인증서 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="667fd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="667fd-107">EXAMPLES</span></span>

### <span data-ttu-id="667fd-108">예제 1: 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="667fd-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="667fd-109">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 일반 텍스트 암호를 안전한 문자열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="667fd-110">명령이 $Password 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="667fd-111">두 번째 명령은 ContosoCertificate 이라는 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="667fd-112">이 명령은 $Password에 저장 된 암호를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="667fd-113">명령은 계정 이름과 업로드 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="667fd-114">변수</span><span class="sxs-lookup"><span data-stu-id="667fd-114">PARAMETERS</span></span>

### <span data-ttu-id="667fd-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="667fd-115">-AutomationAccountName</span></span>
<span data-ttu-id="667fd-116">이 cmdlet이 인증서를 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="667fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667fd-117">-DefaultProfile</span></span>
<span data-ttu-id="667fd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="667fd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="667fd-119">-설명</span><span class="sxs-lookup"><span data-stu-id="667fd-119">-Description</span></span>
<span data-ttu-id="667fd-120">이 cmdlet이 수정 하는 인증서에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="667fd-121">-내보내기 가능한</span><span class="sxs-lookup"><span data-stu-id="667fd-121">-Exportable</span></span>
<span data-ttu-id="667fd-122">인증서를 내보낼 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="667fd-123">-이름</span><span class="sxs-lookup"><span data-stu-id="667fd-123">-Name</span></span>
<span data-ttu-id="667fd-124">이 cmdlet이 수정 하는 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="667fd-125">-암호</span><span class="sxs-lookup"><span data-stu-id="667fd-125">-Password</span></span>
<span data-ttu-id="667fd-126">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="667fd-127">-Path</span><span class="sxs-lookup"><span data-stu-id="667fd-127">-Path</span></span>
<span data-ttu-id="667fd-128">업로드할 스크립트 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="667fd-129">파일은 .cer 파일 또는 .pfx 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="667fd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667fd-130">-ResourceGroupName</span></span>
<span data-ttu-id="667fd-131">이 cmdlet이 인증서를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="667fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667fd-132">CommonParameters</span></span>
<span data-ttu-id="667fd-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="667fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667fd-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667fd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667fd-135">입력</span><span class="sxs-lookup"><span data-stu-id="667fd-135">INPUTS</span></span>

### <span data-ttu-id="667fd-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="667fd-136">System.String</span></span>

### <span data-ttu-id="667fd-137">System.webserver</span><span class="sxs-lookup"><span data-stu-id="667fd-137">System.Security.SecureString</span></span>

### <span data-ttu-id="667fd-138">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="667fd-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="667fd-139">출력</span><span class="sxs-lookup"><span data-stu-id="667fd-139">OUTPUTS</span></span>

### <span data-ttu-id="667fd-140">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="667fd-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="667fd-141">상속자</span><span class="sxs-lookup"><span data-stu-id="667fd-141">NOTES</span></span>

## <span data-ttu-id="667fd-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="667fd-142">RELATED LINKS</span></span>

[<span data-ttu-id="667fd-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="667fd-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="667fd-144">새로운 AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="667fd-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="667fd-145">제거-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="667fd-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


