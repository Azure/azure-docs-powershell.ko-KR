---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526135"
---
# <span data-ttu-id="fd149-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="fd149-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="fd149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd149-102">SYNOPSIS</span></span>
<span data-ttu-id="fd149-103">현재 PowerShell 세션에서 후속 Azure Site Recovery 작업에 사용할 복구 서비스 자격 증명 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd149-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd149-104">SYNTAX</span></span>

### <span data-ttu-id="fd149-105">AzureRecoveryServicesVault (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd149-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd149-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd149-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd149-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd149-107">DESCRIPTION</span></span>
<span data-ttu-id="fd149-108">**AzureRmRecoveryServicesAsrVaultContext** cmdlet은 추가 작업을 위해 Azure Site Recovery 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="fd149-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fd149-109">EXAMPLES</span></span>

### <span data-ttu-id="fd149-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd149-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="fd149-111">현재 PowerShell 세션에서 후속 Azure Site Recovery 작업을 위해 자격 증명 모음 컨텍스트를 지정 된 복구 서비스 자격 증명 모음으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="fd149-112">변수</span><span class="sxs-lookup"><span data-stu-id="fd149-112">PARAMETERS</span></span>

### <span data-ttu-id="fd149-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd149-113">-DefaultProfile</span></span>
<span data-ttu-id="fd149-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd149-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd149-115">-ResourceId</span></span>
<span data-ttu-id="fd149-116">자격 증명 모음 컨텍스트로 설정할 recoveryservices 자격 증명 리소스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd149-117">-저장실</span><span class="sxs-lookup"><span data-stu-id="fd149-117">-Vault</span></span>
<span data-ttu-id="fd149-118">복구 서비스 자격 증명 모음에 해당 하는 Recovery Services 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd149-119">-확인</span><span class="sxs-lookup"><span data-stu-id="fd149-119">-Confirm</span></span>
<span data-ttu-id="fd149-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd149-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd149-121">-WhatIf</span></span>
<span data-ttu-id="fd149-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd149-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd149-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd149-124">CommonParameters</span></span>
<span data-ttu-id="fd149-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd149-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd149-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd149-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd149-127">입력</span><span class="sxs-lookup"><span data-stu-id="fd149-127">INPUTS</span></span>

### <span data-ttu-id="fd149-128">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="fd149-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="fd149-129">출력</span><span class="sxs-lookup"><span data-stu-id="fd149-129">OUTPUTS</span></span>

### <span data-ttu-id="fd149-130">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="fd149-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="fd149-131">상속자</span><span class="sxs-lookup"><span data-stu-id="fd149-131">NOTES</span></span>

## <span data-ttu-id="fd149-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd149-132">RELATED LINKS</span></span>
