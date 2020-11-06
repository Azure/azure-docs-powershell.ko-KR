---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 28a2bb0c806fa152a742c2fc9e36b150116a6352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527539"
---
# <span data-ttu-id="d7c40-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d7c40-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="d7c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c40-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c40-103">메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7c40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7c40-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7c40-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7c40-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c40-106">**AzureKeyVaultCertificateAdministratorDetails** cmdlet은 메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="d7c40-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7c40-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c40-108">예제 1: 인증서 관리자 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d7c40-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="d7c40-109">이 명령은 메모리 내 인증서 관리자 세부 정보 개체를 만든 다음이를 $AdminDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="d7c40-110">변수</span><span class="sxs-lookup"><span data-stu-id="d7c40-110">PARAMETERS</span></span>

### <span data-ttu-id="d7c40-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d7c40-111">-EmailAddress</span></span>
<span data-ttu-id="d7c40-112">인증서 관리자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-112">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="d7c40-113">-FirstName</span><span class="sxs-lookup"><span data-stu-id="d7c40-113">-FirstName</span></span>
<span data-ttu-id="d7c40-114">인증서 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-114">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="d7c40-115">-LastName</span><span class="sxs-lookup"><span data-stu-id="d7c40-115">-LastName</span></span>
<span data-ttu-id="d7c40-116">인증서 관리자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-116">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="d7c40-117">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d7c40-117">-PhoneNumber</span></span>
<span data-ttu-id="d7c40-118">인증서 관리자의 전화 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-118">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="d7c40-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d7c40-119">-Confirm</span></span>
<span data-ttu-id="d7c40-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7c40-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7c40-121">-WhatIf</span></span>
<span data-ttu-id="d7c40-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7c40-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7c40-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c40-124">-DefaultProfile</span></span>
<span data-ttu-id="d7c40-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c40-126">CommonParameters</span></span>
<span data-ttu-id="d7c40-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7c40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c40-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c40-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c40-129">입력</span><span class="sxs-lookup"><span data-stu-id="d7c40-129">INPUTS</span></span>

## <span data-ttu-id="d7c40-130">출력</span><span class="sxs-lookup"><span data-stu-id="d7c40-130">OUTPUTS</span></span>

### <span data-ttu-id="d7c40-131">Microsoft. KeyVault. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d7c40-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="d7c40-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d7c40-132">NOTES</span></span>

## <span data-ttu-id="d7c40-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7c40-133">RELATED LINKS</span></span>

[<span data-ttu-id="d7c40-134">새로운 AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d7c40-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

