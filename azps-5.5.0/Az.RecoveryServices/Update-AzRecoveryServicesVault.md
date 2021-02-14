---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183820"
---
# <span data-ttu-id="57494-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="57494-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="57494-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57494-102">SYNOPSIS</span></span>
<span data-ttu-id="57494-103">MSI를 복구 서비스 자격 증명 모음으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="57494-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="57494-104">구문</span><span class="sxs-lookup"><span data-stu-id="57494-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57494-105">설명</span><span class="sxs-lookup"><span data-stu-id="57494-105">DESCRIPTION</span></span>
<span data-ttu-id="57494-106">이 cmdlet은 복구 서비스 자격 증명 모음에서 MSI를 추가하거나 제거하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="57494-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="57494-107">-IdentityType param을 사용하여 SystemAssigned ID를 RSVault에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="57494-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="57494-108">IdentityType None을 사용하여 자격 증명 모음에서 MSI를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="57494-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="57494-109">예제</span><span class="sxs-lookup"><span data-stu-id="57494-109">EXAMPLES</span></span>

### <span data-ttu-id="57494-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="57494-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="57494-111">이 cmdlet은 Recovery Services 자격 증명 모음에 SystemAssigned ID를 추가하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="57494-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="57494-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57494-112">PARAMETERS</span></span>

### <span data-ttu-id="57494-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57494-113">-DefaultProfile</span></span>
<span data-ttu-id="57494-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57494-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57494-115">-Name</span><span class="sxs-lookup"><span data-stu-id="57494-115">-Name</span></span>

<span data-ttu-id="57494-116">업데이트할 복구 서비스 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57494-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57494-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57494-117">-ResourceGroupName</span></span>

<span data-ttu-id="57494-118">복구 서비스 자격 증명 모음이 있는 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57494-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57494-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="57494-119">-IdentityType</span></span>
<span data-ttu-id="57494-120">Recovery Services 자격 증명 모음에 할당된 MSI 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="57494-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57494-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57494-121">-Confirm</span></span>
<span data-ttu-id="57494-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57494-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57494-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57494-123">-WhatIf</span></span>
<span data-ttu-id="57494-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57494-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57494-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57494-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57494-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57494-126">CommonParameters</span></span>
<span data-ttu-id="57494-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57494-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57494-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57494-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57494-129">입력</span><span class="sxs-lookup"><span data-stu-id="57494-129">INPUTS</span></span>

### <span data-ttu-id="57494-130">System.String</span><span class="sxs-lookup"><span data-stu-id="57494-130">System.String</span></span>

## <span data-ttu-id="57494-131">출력</span><span class="sxs-lookup"><span data-stu-id="57494-131">OUTPUTS</span></span>

### <span data-ttu-id="57494-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="57494-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="57494-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57494-133">NOTES</span></span>

## <span data-ttu-id="57494-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57494-134">RELATED LINKS</span></span>
