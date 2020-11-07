---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 22cc09a405d124ef4bf44342077b53dc64f974b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699105"
---
# <span data-ttu-id="28b14-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="28b14-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="28b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28b14-102">SYNOPSIS</span></span>
<span data-ttu-id="28b14-103">클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="28b14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28b14-104">SYNTAX</span></span>

### <span data-ttu-id="28b14-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="28b14-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b14-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="28b14-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b14-107">설명은</span><span class="sxs-lookup"><span data-stu-id="28b14-107">DESCRIPTION</span></span>
<span data-ttu-id="28b14-108">**AzServiceFabricSetting** 를 사용 하 여 클러스터에서 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="28b14-109">예제의</span><span class="sxs-lookup"><span data-stu-id="28b14-109">EXAMPLES</span></span>

### <span data-ttu-id="28b14-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="28b14-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="28b14-111">이 명령은 ' EseStore ' 섹션에서 ' MaxCursors ' 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="28b14-112">변수</span><span class="sxs-lookup"><span data-stu-id="28b14-112">PARAMETERS</span></span>

### <span data-ttu-id="28b14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b14-113">-DefaultProfile</span></span>
<span data-ttu-id="28b14-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28b14-115">-이름</span><span class="sxs-lookup"><span data-stu-id="28b14-115">-Name</span></span>
<span data-ttu-id="28b14-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="28b14-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="28b14-117">-Parameter</span></span>
<span data-ttu-id="28b14-118">변수도.</span><span class="sxs-lookup"><span data-stu-id="28b14-118">Parameter.</span></span>

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

### <span data-ttu-id="28b14-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b14-119">-ResourceGroupName</span></span>
<span data-ttu-id="28b14-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="28b14-121">-섹션</span><span class="sxs-lookup"><span data-stu-id="28b14-121">-Section</span></span>
<span data-ttu-id="28b14-122">여기.</span><span class="sxs-lookup"><span data-stu-id="28b14-122">Section.</span></span>

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

### <span data-ttu-id="28b14-123">-Settings섹션 설명</span><span class="sxs-lookup"><span data-stu-id="28b14-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="28b14-124">클라이언트 인증 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-124">Client authentication type.</span></span>

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

### <span data-ttu-id="28b14-125">-확인</span><span class="sxs-lookup"><span data-stu-id="28b14-125">-Confirm</span></span>
<span data-ttu-id="28b14-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b14-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b14-127">-WhatIf</span></span>
<span data-ttu-id="28b14-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28b14-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b14-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b14-130">CommonParameters</span></span>
<span data-ttu-id="28b14-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b14-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b14-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b14-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b14-133">입력</span><span class="sxs-lookup"><span data-stu-id="28b14-133">INPUTS</span></span>

### <span data-ttu-id="28b14-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28b14-134">System.String</span></span>

### <span data-ttu-id="28b14-135">ServiceFabric. Pssettings섹션 설명 []</span><span class="sxs-lookup"><span data-stu-id="28b14-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="28b14-136">출력</span><span class="sxs-lookup"><span data-stu-id="28b14-136">OUTPUTS</span></span>

### <span data-ttu-id="28b14-137">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="28b14-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="28b14-138">상속자</span><span class="sxs-lookup"><span data-stu-id="28b14-138">NOTES</span></span>

## <span data-ttu-id="28b14-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28b14-139">RELATED LINKS</span></span>
