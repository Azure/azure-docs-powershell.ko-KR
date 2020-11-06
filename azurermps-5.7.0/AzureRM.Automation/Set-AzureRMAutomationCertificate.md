---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: a1858419b20bf85a40f94e2b5016b461cd24c39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533791"
---
# <span data-ttu-id="80dea-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="80dea-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="80dea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80dea-102">SYNOPSIS</span></span>
<span data-ttu-id="80dea-103">자동화 인증서의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80dea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80dea-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80dea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80dea-105">DESCRIPTION</span></span>
<span data-ttu-id="80dea-106">**AzureRmAutomationCertificate** Cmdlet은 Azure Automation에서 인증서 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="80dea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="80dea-107">EXAMPLES</span></span>

### <span data-ttu-id="80dea-108">예제 1: 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="80dea-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="80dea-109">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 일반 텍스트 암호를 안전한 문자열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="80dea-110">명령이 $Password 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="80dea-111">두 번째 명령은 ContosoCertificate 이라는 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="80dea-112">이 명령은 $Password에 저장 된 암호를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="80dea-113">명령은 계정 이름과 업로드 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="80dea-114">변수</span><span class="sxs-lookup"><span data-stu-id="80dea-114">PARAMETERS</span></span>

### <span data-ttu-id="80dea-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="80dea-115">-AutomationAccountName</span></span>
<span data-ttu-id="80dea-116">이 cmdlet이 인증서를 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80dea-117">-DefaultProfile</span></span>
<span data-ttu-id="80dea-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="80dea-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-119">-설명</span><span class="sxs-lookup"><span data-stu-id="80dea-119">-Description</span></span>
<span data-ttu-id="80dea-120">이 cmdlet이 수정 하는 인증서에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-121">-내보내기 가능한</span><span class="sxs-lookup"><span data-stu-id="80dea-121">-Exportable</span></span>
<span data-ttu-id="80dea-122">인증서를 내보낼 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-123">-이름</span><span class="sxs-lookup"><span data-stu-id="80dea-123">-Name</span></span>
<span data-ttu-id="80dea-124">이 cmdlet이 수정 하는 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-125">-암호</span><span class="sxs-lookup"><span data-stu-id="80dea-125">-Password</span></span>
<span data-ttu-id="80dea-126">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-127">-Path</span><span class="sxs-lookup"><span data-stu-id="80dea-127">-Path</span></span>
<span data-ttu-id="80dea-128">업로드할 스크립트 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="80dea-129">파일은 .cer 파일 또는 .pfx 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-129">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80dea-130">-ResourceGroupName</span></span>
<span data-ttu-id="80dea-131">이 cmdlet이 인증서를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80dea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dea-132">CommonParameters</span></span>
<span data-ttu-id="80dea-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80dea-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80dea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dea-135">입력</span><span class="sxs-lookup"><span data-stu-id="80dea-135">INPUTS</span></span>

### <span data-ttu-id="80dea-136">않아야</span><span class="sxs-lookup"><span data-stu-id="80dea-136">None</span></span>
<span data-ttu-id="80dea-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80dea-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80dea-138">출력</span><span class="sxs-lookup"><span data-stu-id="80dea-138">OUTPUTS</span></span>

### <span data-ttu-id="80dea-139">Microsoft. Azure. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="80dea-139">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="80dea-140">상속자</span><span class="sxs-lookup"><span data-stu-id="80dea-140">NOTES</span></span>

## <span data-ttu-id="80dea-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80dea-141">RELATED LINKS</span></span>

[<span data-ttu-id="80dea-142">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="80dea-142">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="80dea-143">새로운 AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="80dea-143">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="80dea-144">제거-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="80dea-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


