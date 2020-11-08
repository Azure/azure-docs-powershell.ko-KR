---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 943edbccfa8ae8e264d4058deac0407a535c614c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034056"
---
# <span data-ttu-id="15a03-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="15a03-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="15a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a03-102">SYNOPSIS</span></span>
<span data-ttu-id="15a03-103">클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="15a03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15a03-104">SYNTAX</span></span>

### <span data-ttu-id="15a03-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="15a03-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a03-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="15a03-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a03-107">설명은</span><span class="sxs-lookup"><span data-stu-id="15a03-107">DESCRIPTION</span></span>
<span data-ttu-id="15a03-108">**AzServiceFabricSetting** 를 사용 하 여 클러스터에서 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="15a03-109">예제의</span><span class="sxs-lookup"><span data-stu-id="15a03-109">EXAMPLES</span></span>

### <span data-ttu-id="15a03-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="15a03-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="15a03-111">이 명령은 ' EseStore ' 섹션에서 ' MaxCursors ' 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="15a03-112">변수</span><span class="sxs-lookup"><span data-stu-id="15a03-112">PARAMETERS</span></span>

### <span data-ttu-id="15a03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a03-113">-DefaultProfile</span></span>
<span data-ttu-id="15a03-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a03-115">-이름</span><span class="sxs-lookup"><span data-stu-id="15a03-115">-Name</span></span>
<span data-ttu-id="15a03-116">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="15a03-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="15a03-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="15a03-117">-Parameter</span></span>
<span data-ttu-id="15a03-118">패브릭 설정의 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="15a03-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="15a03-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a03-119">-ResourceGroupName</span></span>
<span data-ttu-id="15a03-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="15a03-121">-섹션</span><span class="sxs-lookup"><span data-stu-id="15a03-121">-Section</span></span>
<span data-ttu-id="15a03-122">패브릭 설정의 섹션 이름</span><span class="sxs-lookup"><span data-stu-id="15a03-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="15a03-123">-Settings섹션 설명</span><span class="sxs-lookup"><span data-stu-id="15a03-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="15a03-124">패브릭 설정의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="15a03-125">-확인</span><span class="sxs-lookup"><span data-stu-id="15a03-125">-Confirm</span></span>
<span data-ttu-id="15a03-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a03-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a03-127">-WhatIf</span></span>
<span data-ttu-id="15a03-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a03-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a03-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a03-130">CommonParameters</span></span>
<span data-ttu-id="15a03-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a03-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a03-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a03-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a03-133">입력</span><span class="sxs-lookup"><span data-stu-id="15a03-133">INPUTS</span></span>

### <span data-ttu-id="15a03-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15a03-134">System.String</span></span>

### <span data-ttu-id="15a03-135">ServiceFabric. Pssettings섹션 설명 []</span><span class="sxs-lookup"><span data-stu-id="15a03-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="15a03-136">출력</span><span class="sxs-lookup"><span data-stu-id="15a03-136">OUTPUTS</span></span>

### <span data-ttu-id="15a03-137">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="15a03-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="15a03-138">상속자</span><span class="sxs-lookup"><span data-stu-id="15a03-138">NOTES</span></span>

## <span data-ttu-id="15a03-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15a03-139">RELATED LINKS</span></span>
