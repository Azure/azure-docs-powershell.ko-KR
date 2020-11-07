---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 4643ab29be9c93f58895048317edc2b1db6115e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704115"
---
# <span data-ttu-id="2b87d-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2b87d-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="2b87d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b87d-102">SYNOPSIS</span></span>
<span data-ttu-id="2b87d-103">클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b87d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b87d-104">SYNTAX</span></span>

### <span data-ttu-id="2b87d-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="2b87d-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b87d-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="2b87d-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b87d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2b87d-107">DESCRIPTION</span></span>
<span data-ttu-id="2b87d-108">**AzureRmServiceFabricSetting** 를 사용 하 여 클러스터에서 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="2b87d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2b87d-109">EXAMPLES</span></span>

### <span data-ttu-id="2b87d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b87d-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="2b87d-111">이 명령은 ' EseStore ' 섹션에서 ' MaxCursors ' 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="2b87d-112">변수</span><span class="sxs-lookup"><span data-stu-id="2b87d-112">PARAMETERS</span></span>

### <span data-ttu-id="2b87d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b87d-113">-DefaultProfile</span></span>
<span data-ttu-id="2b87d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b87d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="2b87d-115">-Name</span></span>
<span data-ttu-id="2b87d-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b87d-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2b87d-117">-Parameter</span></span>
<span data-ttu-id="2b87d-118">변수도.</span><span class="sxs-lookup"><span data-stu-id="2b87d-118">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b87d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b87d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b87d-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b87d-121">-섹션</span><span class="sxs-lookup"><span data-stu-id="2b87d-121">-Section</span></span>
<span data-ttu-id="2b87d-122">여기.</span><span class="sxs-lookup"><span data-stu-id="2b87d-122">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b87d-123">-Settings섹션 설명</span><span class="sxs-lookup"><span data-stu-id="2b87d-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="2b87d-124">클라이언트 인증 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-124">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b87d-125">-확인</span><span class="sxs-lookup"><span data-stu-id="2b87d-125">-Confirm</span></span>
<span data-ttu-id="2b87d-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b87d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b87d-127">-WhatIf</span></span>
<span data-ttu-id="2b87d-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b87d-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b87d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b87d-130">CommonParameters</span></span>
<span data-ttu-id="2b87d-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b87d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b87d-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b87d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b87d-133">입력</span><span class="sxs-lookup"><span data-stu-id="2b87d-133">INPUTS</span></span>

### <span data-ttu-id="2b87d-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b87d-134">System.String</span></span>
<span data-ttu-id="2b87d-135">매개 변수: 매개 변수 (ByValue), Section (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2b87d-135">Parameters: Parameter (ByValue), Section (ByValue)</span></span>

### <span data-ttu-id="2b87d-136">ServiceFabric. Pssettings섹션 설명 []</span><span class="sxs-lookup"><span data-stu-id="2b87d-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="2b87d-137">매개 변수: Settings섹션 설명 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2b87d-137">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="2b87d-138">출력</span><span class="sxs-lookup"><span data-stu-id="2b87d-138">OUTPUTS</span></span>

### <span data-ttu-id="2b87d-139">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="2b87d-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2b87d-140">상속자</span><span class="sxs-lookup"><span data-stu-id="2b87d-140">NOTES</span></span>

## <span data-ttu-id="2b87d-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b87d-141">RELATED LINKS</span></span>
