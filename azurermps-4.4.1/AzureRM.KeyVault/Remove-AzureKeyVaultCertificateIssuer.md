---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534951"
---
# <span data-ttu-id="4cdc5-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4cdc5-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4cdc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cdc5-102">SYNOPSIS</span></span>
<span data-ttu-id="4cdc5-103">키 자격 증명 모음에서 인증서 발급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cdc5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cdc5-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cdc5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4cdc5-105">DESCRIPTION</span></span>
<span data-ttu-id="4cdc5-106">**AzureKeyVaultCertificateIssuer** cmdlet은 키 자격 증명 모음에서 인증서 발급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="4cdc5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4cdc5-107">EXAMPLES</span></span>

### <span data-ttu-id="4cdc5-108">예제 1: 인증서 발급자 제거</span><span class="sxs-lookup"><span data-stu-id="4cdc5-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="4cdc5-109">이 명령은 ContosoKV01 키 자격 증명 모음에서 TestIssuer01 이라는 인증서 발급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="4cdc5-110">변수</span><span class="sxs-lookup"><span data-stu-id="4cdc5-110">PARAMETERS</span></span>

### <span data-ttu-id="4cdc5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4cdc5-111">-Force</span></span>
<span data-ttu-id="4cdc5-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdc5-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4cdc5-113">-Name</span></span>
<span data-ttu-id="4cdc5-114">제거할 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cdc5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cdc5-115">-PassThru</span></span>
<span data-ttu-id="4cdc5-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4cdc5-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdc5-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4cdc5-118">-VaultName</span></span>
<span data-ttu-id="4cdc5-119">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4cdc5-120">-확인</span><span class="sxs-lookup"><span data-stu-id="4cdc5-120">-Confirm</span></span>
<span data-ttu-id="4cdc5-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdc5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cdc5-122">-WhatIf</span></span>
<span data-ttu-id="4cdc5-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cdc5-124">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cdc5-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdc5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cdc5-126">-DefaultProfile</span></span>
<span data-ttu-id="4cdc5-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cdc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cdc5-128">CommonParameters</span></span>
<span data-ttu-id="4cdc5-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cdc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cdc5-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cdc5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cdc5-131">입력</span><span class="sxs-lookup"><span data-stu-id="4cdc5-131">INPUTS</span></span>

## <span data-ttu-id="4cdc5-132">출력</span><span class="sxs-lookup"><span data-stu-id="4cdc5-132">OUTPUTS</span></span>

### <span data-ttu-id="4cdc5-133">Microsoft. KeyVault. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4cdc5-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4cdc5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4cdc5-134">NOTES</span></span>

## <span data-ttu-id="4cdc5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cdc5-135">RELATED LINKS</span></span>

[<span data-ttu-id="4cdc5-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4cdc5-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="4cdc5-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4cdc5-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


