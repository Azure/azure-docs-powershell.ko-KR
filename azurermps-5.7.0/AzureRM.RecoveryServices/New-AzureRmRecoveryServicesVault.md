---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 3abb13803dbe564eb7562691b10a453174374444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533668"
---
# <span data-ttu-id="c153e-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c153e-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="c153e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c153e-102">SYNOPSIS</span></span>
<span data-ttu-id="c153e-103">새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c153e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c153e-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c153e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c153e-105">DESCRIPTION</span></span>
<span data-ttu-id="c153e-106">**AzureRmRecoveryServicesVault** cmdlet은 새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="c153e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c153e-107">EXAMPLES</span></span>

### <span data-ttu-id="c153e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c153e-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="c153e-109">리소스 그룹 및 지정 된 위치에 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="c153e-110">변수</span><span class="sxs-lookup"><span data-stu-id="c153e-110">PARAMETERS</span></span>

### <span data-ttu-id="c153e-111">-위치</span><span class="sxs-lookup"><span data-stu-id="c153e-111">-Location</span></span>
<span data-ttu-id="c153e-112">자격 증명 모음의 지리적 위치 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c153e-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c153e-113">-Name</span></span>
<span data-ttu-id="c153e-114">만들 저장실의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c153e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c153e-115">-ResourceGroupName</span></span>
<span data-ttu-id="c153e-116">지정 된 복구 서비스 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c153e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="c153e-117">-Confirm</span></span>
<span data-ttu-id="c153e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c153e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c153e-119">-WhatIf</span></span>
<span data-ttu-id="c153e-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c153e-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c153e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c153e-122">-DefaultProfile</span></span>
<span data-ttu-id="c153e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c153e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c153e-124">CommonParameters</span></span>
<span data-ttu-id="c153e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c153e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c153e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c153e-127">입력</span><span class="sxs-lookup"><span data-stu-id="c153e-127">INPUTS</span></span>

### <span data-ttu-id="c153e-128">않아야</span><span class="sxs-lookup"><span data-stu-id="c153e-128">None</span></span>
<span data-ttu-id="c153e-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c153e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c153e-130">출력</span><span class="sxs-lookup"><span data-stu-id="c153e-130">OUTPUTS</span></span>

### <span data-ttu-id="c153e-131">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="c153e-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="c153e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c153e-132">NOTES</span></span>

## <span data-ttu-id="c153e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c153e-133">RELATED LINKS</span></span>

[<span data-ttu-id="c153e-134">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c153e-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="c153e-135">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c153e-135">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="c153e-136">제거-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c153e-136">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


