---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699624"
---
# <span data-ttu-id="c0be8-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="c0be8-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="c0be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0be8-102">SYNOPSIS</span></span>
<span data-ttu-id="c0be8-103">ASR 패브릭에서 vCenter server를 제거 하 고 vCenter 서버에서 가상 컴퓨터의 검색을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="c0be8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0be8-104">SYNTAX</span></span>

### <span data-ttu-id="c0be8-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0be8-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0be8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0be8-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0be8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c0be8-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0be8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c0be8-108">DESCRIPTION</span></span>
<span data-ttu-id="c0be8-109">**AzRecoveryServicesAsrvCenter** CMDLET은 ASR 패브릭에서 vcenter server를 제거 하 고 vcenter 서버에서 가상 컴퓨터의 검색을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="c0be8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c0be8-110">EXAMPLES</span></span>

### <span data-ttu-id="c0be8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0be8-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="c0be8-112">ASR 패브릭에서 vCenter 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="c0be8-113">변수</span><span class="sxs-lookup"><span data-stu-id="c0be8-113">PARAMETERS</span></span>

### <span data-ttu-id="c0be8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0be8-114">-DefaultProfile</span></span>
<span data-ttu-id="c0be8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0be8-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="c0be8-116">-Fabric</span></span>
<span data-ttu-id="c0be8-117">구성 서버를 나타내는 ASR fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0be8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0be8-118">-InputObject</span></span>
<span data-ttu-id="c0be8-119">제거할 vCenter server를 나타내는 ASR vCenter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="c0be8-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c0be8-120">-Name</span></span>
<span data-ttu-id="c0be8-121">VCenter 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0be8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0be8-122">-ResourceId</span></span>
<span data-ttu-id="c0be8-123">제거할 vCenter의 resourceId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="c0be8-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c0be8-124">-Confirm</span></span>
<span data-ttu-id="c0be8-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0be8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0be8-126">-WhatIf</span></span>
<span data-ttu-id="c0be8-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0be8-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0be8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0be8-129">CommonParameters</span></span>
<span data-ttu-id="c0be8-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0be8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0be8-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0be8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0be8-132">입력</span><span class="sxs-lookup"><span data-stu-id="c0be8-132">INPUTS</span></span>

### <span data-ttu-id="c0be8-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0be8-133">System.String</span></span>

### <span data-ttu-id="c0be8-134">SiteRecovery. r m/$ 명령</span><span class="sxs-lookup"><span data-stu-id="c0be8-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="c0be8-135">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="c0be8-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c0be8-136">출력</span><span class="sxs-lookup"><span data-stu-id="c0be8-136">OUTPUTS</span></span>

### <span data-ttu-id="c0be8-137">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="c0be8-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c0be8-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c0be8-138">NOTES</span></span>

## <span data-ttu-id="c0be8-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0be8-139">RELATED LINKS</span></span>
