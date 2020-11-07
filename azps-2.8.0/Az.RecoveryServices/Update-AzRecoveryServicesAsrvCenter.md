---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d6e26eb293a2b87fccc0749b6d5c53d15d7d860f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873463"
---
# <span data-ttu-id="3c64a-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="3c64a-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="3c64a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c64a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c64a-103">등록 된 vCenter에 대 한 검색 세부 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="3c64a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c64a-104">SYNTAX</span></span>

### <span data-ttu-id="3c64a-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3c64a-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c64a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c64a-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c64a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3c64a-107">DESCRIPTION</span></span>
<span data-ttu-id="3c64a-108">**업데이트 AzRecoveryServicesAsrvCenter** cmdlet은 등록 된 vCenter에 대 한 검색 세부 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="3c64a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3c64a-109">EXAMPLES</span></span>

### <span data-ttu-id="3c64a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c64a-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="3c64a-111">등록 된 vCenter에 대 한 검색 세부 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="3c64a-112">변수</span><span class="sxs-lookup"><span data-stu-id="3c64a-112">PARAMETERS</span></span>

### <span data-ttu-id="3c64a-113">-계정</span><span class="sxs-lookup"><span data-stu-id="3c64a-113">-Account</span></span>
<span data-ttu-id="3c64a-114">vCenter login 자격 증명 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c64a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c64a-115">-DefaultProfile</span></span>
<span data-ttu-id="3c64a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c64a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c64a-117">-InputObject</span></span>
<span data-ttu-id="3c64a-118">검색 세부 정보를 업데이트할 vCenter server 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c64a-119">-포트</span><span class="sxs-lookup"><span data-stu-id="3c64a-119">-Port</span></span>
<span data-ttu-id="3c64a-120">검색에 사용할 vCenter 서버의 TCP 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c64a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c64a-121">-ResourceId</span></span>
<span data-ttu-id="3c64a-122">VCenter의 resourceId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="3c64a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="3c64a-123">-Confirm</span></span>
<span data-ttu-id="3c64a-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c64a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c64a-125">-WhatIf</span></span>
<span data-ttu-id="3c64a-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c64a-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c64a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c64a-128">CommonParameters</span></span>
<span data-ttu-id="3c64a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c64a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c64a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c64a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c64a-131">입력</span><span class="sxs-lookup"><span data-stu-id="3c64a-131">INPUTS</span></span>

### <span data-ttu-id="3c64a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3c64a-132">System.String</span></span>

### <span data-ttu-id="3c64a-133">SiteRecovery. r m/$ 명령</span><span class="sxs-lookup"><span data-stu-id="3c64a-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="3c64a-134">출력</span><span class="sxs-lookup"><span data-stu-id="3c64a-134">OUTPUTS</span></span>

### <span data-ttu-id="3c64a-135">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="3c64a-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3c64a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3c64a-136">NOTES</span></span>

## <span data-ttu-id="3c64a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c64a-137">RELATED LINKS</span></span>
