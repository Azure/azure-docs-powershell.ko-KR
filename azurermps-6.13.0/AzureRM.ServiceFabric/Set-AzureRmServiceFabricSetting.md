---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 42d643faa1b3047c6ee2e3266a68a2ce692ec676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530888"
---
# <span data-ttu-id="72bd9-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="72bd9-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="72bd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="72bd9-103">하나 또는 여러 개의 서비스 패브릭 설정을 클러스터에 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72bd9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72bd9-104">SYNTAX</span></span>

### <span data-ttu-id="72bd9-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="72bd9-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72bd9-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="72bd9-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72bd9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="72bd9-107">DESCRIPTION</span></span>
<span data-ttu-id="72bd9-108">**AzureRmServiceFabricSetting** 를 사용 하 여 클러스터에서 서비스 패브릭 설정을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="72bd9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="72bd9-109">EXAMPLES</span></span>

### <span data-ttu-id="72bd9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="72bd9-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="72bd9-111">이 명령은 ' NamingService ' 섹션에서 ' MaxFileOperationTimeout '을 ' 5000 ' 값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="72bd9-112">변수</span><span class="sxs-lookup"><span data-stu-id="72bd9-112">PARAMETERS</span></span>

### <span data-ttu-id="72bd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bd9-113">-DefaultProfile</span></span>
<span data-ttu-id="72bd9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72bd9-115">-이름</span><span class="sxs-lookup"><span data-stu-id="72bd9-115">-Name</span></span>
<span data-ttu-id="72bd9-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="72bd9-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="72bd9-117">-Parameter</span></span>
<span data-ttu-id="72bd9-118">변수도.</span><span class="sxs-lookup"><span data-stu-id="72bd9-118">Parameter.</span></span>

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

### <span data-ttu-id="72bd9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72bd9-119">-ResourceGroupName</span></span>
<span data-ttu-id="72bd9-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="72bd9-121">-섹션</span><span class="sxs-lookup"><span data-stu-id="72bd9-121">-Section</span></span>
<span data-ttu-id="72bd9-122">여기.</span><span class="sxs-lookup"><span data-stu-id="72bd9-122">Section.</span></span>

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

### <span data-ttu-id="72bd9-123">-Settings섹션 설명</span><span class="sxs-lookup"><span data-stu-id="72bd9-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="72bd9-124">클라이언트 인증 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-124">Client authentication type.</span></span>

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

### <span data-ttu-id="72bd9-125">-값</span><span class="sxs-lookup"><span data-stu-id="72bd9-125">-Value</span></span>
<span data-ttu-id="72bd9-126">값.</span><span class="sxs-lookup"><span data-stu-id="72bd9-126">Value.</span></span>

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

### <span data-ttu-id="72bd9-127">-확인</span><span class="sxs-lookup"><span data-stu-id="72bd9-127">-Confirm</span></span>
<span data-ttu-id="72bd9-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72bd9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72bd9-129">-WhatIf</span></span>
<span data-ttu-id="72bd9-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72bd9-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72bd9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bd9-132">CommonParameters</span></span>
<span data-ttu-id="72bd9-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bd9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bd9-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72bd9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bd9-135">입력</span><span class="sxs-lookup"><span data-stu-id="72bd9-135">INPUTS</span></span>

### <span data-ttu-id="72bd9-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72bd9-136">System.String</span></span>
<span data-ttu-id="72bd9-137">매개 변수: 매개 변수 (ByValue), Section (ByValue), Value (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72bd9-137">Parameters: Parameter (ByValue), Section (ByValue), Value (ByValue)</span></span>

### <span data-ttu-id="72bd9-138">ServiceFabric. Pssettings섹션 설명 []</span><span class="sxs-lookup"><span data-stu-id="72bd9-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="72bd9-139">매개 변수: Settings섹션 설명 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72bd9-139">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="72bd9-140">출력</span><span class="sxs-lookup"><span data-stu-id="72bd9-140">OUTPUTS</span></span>

### <span data-ttu-id="72bd9-141">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="72bd9-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="72bd9-142">상속자</span><span class="sxs-lookup"><span data-stu-id="72bd9-142">NOTES</span></span>

## <span data-ttu-id="72bd9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72bd9-143">RELATED LINKS</span></span>
