---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034146"
---
# <span data-ttu-id="dca28-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="dca28-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="dca28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca28-102">SYNOPSIS</span></span>
<span data-ttu-id="dca28-103">메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="dca28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dca28-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dca28-105">DESCRIPTION</span></span>
<span data-ttu-id="dca28-106">**AzKeyVaultCertificateAdministratorDetail** cmdlet은 메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="dca28-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dca28-107">EXAMPLES</span></span>

### <span data-ttu-id="dca28-108">예제 1: 인증서 관리자 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="dca28-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="dca28-109">이 명령은 메모리 내 인증서 관리자 세부 정보 개체를 만든 다음이를 $AdminDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="dca28-110">변수</span><span class="sxs-lookup"><span data-stu-id="dca28-110">PARAMETERS</span></span>

### <span data-ttu-id="dca28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca28-111">-DefaultProfile</span></span>
<span data-ttu-id="dca28-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dca28-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dca28-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="dca28-113">-EmailAddress</span></span>
<span data-ttu-id="dca28-114">인증서 관리자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="dca28-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="dca28-115">-FirstName</span></span>
<span data-ttu-id="dca28-116">인증서 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="dca28-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="dca28-117">-LastName</span></span>
<span data-ttu-id="dca28-118">인증서 관리자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="dca28-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="dca28-119">-PhoneNumber</span></span>
<span data-ttu-id="dca28-120">인증서 관리자의 전화 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="dca28-121">-확인</span><span class="sxs-lookup"><span data-stu-id="dca28-121">-Confirm</span></span>
<span data-ttu-id="dca28-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca28-123">-WhatIf</span></span>
<span data-ttu-id="dca28-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca28-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca28-126">CommonParameters</span></span>
<span data-ttu-id="dca28-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dca28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca28-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dca28-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca28-129">입력</span><span class="sxs-lookup"><span data-stu-id="dca28-129">INPUTS</span></span>

### <span data-ttu-id="dca28-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dca28-130">System.String</span></span>

## <span data-ttu-id="dca28-131">출력</span><span class="sxs-lookup"><span data-stu-id="dca28-131">OUTPUTS</span></span>

### <span data-ttu-id="dca28-132">Microsoft. KeyVault. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="dca28-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="dca28-133">상속자</span><span class="sxs-lookup"><span data-stu-id="dca28-133">NOTES</span></span>

## <span data-ttu-id="dca28-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dca28-134">RELATED LINKS</span></span>

[<span data-ttu-id="dca28-135">새로운 AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="dca28-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

