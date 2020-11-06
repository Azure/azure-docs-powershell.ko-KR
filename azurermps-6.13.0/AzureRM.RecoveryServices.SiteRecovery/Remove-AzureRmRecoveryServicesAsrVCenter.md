---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535148"
---
# <span data-ttu-id="d430b-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="d430b-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="d430b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d430b-102">SYNOPSIS</span></span>
<span data-ttu-id="d430b-103">ASR 패브릭에서 vCenter server를 제거 하 고 vCenter 서버에서 가상 컴퓨터의 검색을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d430b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d430b-104">SYNTAX</span></span>

### <span data-ttu-id="d430b-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d430b-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d430b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d430b-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d430b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d430b-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d430b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d430b-108">DESCRIPTION</span></span>
<span data-ttu-id="d430b-109">**AzureRmRecoveryServicesAsrvCenter** CMDLET은 ASR 패브릭에서 vcenter server를 제거 하 고 vcenter 서버에서 가상 컴퓨터의 검색을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="d430b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d430b-110">EXAMPLES</span></span>

### <span data-ttu-id="d430b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d430b-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="d430b-112">ASR 패브릭에서 vCenter 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="d430b-113">변수</span><span class="sxs-lookup"><span data-stu-id="d430b-113">PARAMETERS</span></span>

### <span data-ttu-id="d430b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d430b-114">-DefaultProfile</span></span>
<span data-ttu-id="d430b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d430b-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="d430b-116">-Fabric</span></span>
<span data-ttu-id="d430b-117">구성 서버를 나타내는 ASR fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="d430b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d430b-118">-InputObject</span></span>
<span data-ttu-id="d430b-119">제거할 vCenter server를 나타내는 ASR vCenter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="d430b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d430b-120">-Name</span></span>
<span data-ttu-id="d430b-121">VCenter 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="d430b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d430b-122">-ResourceId</span></span>
<span data-ttu-id="d430b-123">제거할 vCenter의 resourceId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="d430b-124">-확인</span><span class="sxs-lookup"><span data-stu-id="d430b-124">-Confirm</span></span>
<span data-ttu-id="d430b-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d430b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d430b-126">-WhatIf</span></span>
<span data-ttu-id="d430b-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d430b-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d430b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d430b-129">CommonParameters</span></span>
<span data-ttu-id="d430b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d430b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d430b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d430b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d430b-132">입력</span><span class="sxs-lookup"><span data-stu-id="d430b-132">INPUTS</span></span>

### <span data-ttu-id="d430b-133">SiteRecovery. r m/$ 명령</span><span class="sxs-lookup"><span data-stu-id="d430b-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="d430b-134">출력</span><span class="sxs-lookup"><span data-stu-id="d430b-134">OUTPUTS</span></span>

### <span data-ttu-id="d430b-135">System.webserver. t e r ' 1 [[SiteRecovery Rjob], [[Microsoft Azure. SiteRecovery, Version = 0.1.1.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="d430b-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d430b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="d430b-136">NOTES</span></span>

## <span data-ttu-id="d430b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d430b-137">RELATED LINKS</span></span>
