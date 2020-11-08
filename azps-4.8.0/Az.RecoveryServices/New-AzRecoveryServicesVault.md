---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214259"
---
# <span data-ttu-id="187fc-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="187fc-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="187fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="187fc-102">SYNOPSIS</span></span>
<span data-ttu-id="187fc-103">새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="187fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="187fc-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="187fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="187fc-105">DESCRIPTION</span></span>
<span data-ttu-id="187fc-106">**AzRecoveryServicesVault** cmdlet은 새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="187fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="187fc-107">EXAMPLES</span></span>

### <span data-ttu-id="187fc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="187fc-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="187fc-109">리소스 그룹 및 지정 된 위치에 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="187fc-110">변수</span><span class="sxs-lookup"><span data-stu-id="187fc-110">PARAMETERS</span></span>

### <span data-ttu-id="187fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187fc-111">-DefaultProfile</span></span>
<span data-ttu-id="187fc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="187fc-113">-위치</span><span class="sxs-lookup"><span data-stu-id="187fc-113">-Location</span></span>
<span data-ttu-id="187fc-114">자격 증명 모음의 지리적 위치 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-114">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187fc-115">-이름</span><span class="sxs-lookup"><span data-stu-id="187fc-115">-Name</span></span>
<span data-ttu-id="187fc-116">만들 저장실의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-116">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187fc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187fc-117">-ResourceGroupName</span></span>
<span data-ttu-id="187fc-118">지정 된 복구 서비스 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187fc-119">태그</span><span class="sxs-lookup"><span data-stu-id="187fc-119">-Tag</span></span>

<span data-ttu-id="187fc-120">복구 서비스 자격 증명 모음에 추가할 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187fc-121">-확인</span><span class="sxs-lookup"><span data-stu-id="187fc-121">-Confirm</span></span>
<span data-ttu-id="187fc-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="187fc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187fc-123">-WhatIf</span></span>
<span data-ttu-id="187fc-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="187fc-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="187fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187fc-126">CommonParameters</span></span>
<span data-ttu-id="187fc-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187fc-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="187fc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187fc-129">입력</span><span class="sxs-lookup"><span data-stu-id="187fc-129">INPUTS</span></span>

### <span data-ttu-id="187fc-130">않아야</span><span class="sxs-lookup"><span data-stu-id="187fc-130">None</span></span>

## <span data-ttu-id="187fc-131">출력</span><span class="sxs-lookup"><span data-stu-id="187fc-131">OUTPUTS</span></span>

### <span data-ttu-id="187fc-132">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="187fc-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="187fc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="187fc-133">NOTES</span></span>

## <span data-ttu-id="187fc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="187fc-134">RELATED LINKS</span></span>

[<span data-ttu-id="187fc-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="187fc-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="187fc-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="187fc-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="187fc-137">제거-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="187fc-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


