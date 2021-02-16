---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200017"
---
# <span data-ttu-id="9dc73-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="9dc73-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="9dc73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dc73-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc73-103">메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="9dc73-104">구문</span><span class="sxs-lookup"><span data-stu-id="9dc73-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc73-105">설명</span><span class="sxs-lookup"><span data-stu-id="9dc73-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc73-106">**New-AzKeyVaultCertificateAdministratorDetail** cmdlet은 메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="9dc73-107">예제</span><span class="sxs-lookup"><span data-stu-id="9dc73-107">EXAMPLES</span></span>

### <span data-ttu-id="9dc73-108">예제 1: 인증서 관리자 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9dc73-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="9dc73-109">이 명령은 메모리 내 인증서 관리자 세부 정보 개체를 만든 다음, $AdminDetails 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="9dc73-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dc73-110">PARAMETERS</span></span>

### <span data-ttu-id="9dc73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc73-111">-DefaultProfile</span></span>
<span data-ttu-id="9dc73-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9dc73-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dc73-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9dc73-113">-EmailAddress</span></span>
<span data-ttu-id="9dc73-114">인증서 관리자의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="9dc73-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="9dc73-115">-FirstName</span></span>
<span data-ttu-id="9dc73-116">인증서 관리자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="9dc73-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="9dc73-117">-LastName</span></span>
<span data-ttu-id="9dc73-118">인증서 관리자의 성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="9dc73-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9dc73-119">-PhoneNumber</span></span>
<span data-ttu-id="9dc73-120">인증서 관리자의 전화 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="9dc73-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dc73-121">-Confirm</span></span>
<span data-ttu-id="9dc73-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc73-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc73-123">-WhatIf</span></span>
<span data-ttu-id="9dc73-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9dc73-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc73-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc73-126">CommonParameters</span></span>
<span data-ttu-id="9dc73-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc73-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9dc73-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc73-129">입력</span><span class="sxs-lookup"><span data-stu-id="9dc73-129">INPUTS</span></span>

### <span data-ttu-id="9dc73-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9dc73-130">System.String</span></span>

## <span data-ttu-id="9dc73-131">출력</span><span class="sxs-lookup"><span data-stu-id="9dc73-131">OUTPUTS</span></span>

### <span data-ttu-id="9dc73-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="9dc73-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="9dc73-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9dc73-133">NOTES</span></span>

## <span data-ttu-id="9dc73-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9dc73-134">RELATED LINKS</span></span>

[<span data-ttu-id="9dc73-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="9dc73-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

