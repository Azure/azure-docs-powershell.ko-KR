---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 72a538c039914eebdcd2926cda93a97cfe2d267a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212140"
---
# <span data-ttu-id="be5c7-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="be5c7-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="be5c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="be5c7-103">하나 또는 여러 개의 서비스 패브릭 설정을 클러스터에 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="be5c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be5c7-104">SYNTAX</span></span>

### <span data-ttu-id="be5c7-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="be5c7-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be5c7-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="be5c7-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be5c7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="be5c7-107">DESCRIPTION</span></span>
<span data-ttu-id="be5c7-108">**AzServiceFabricSetting** 를 사용 하 여 클러스터에서 서비스 패브릭 설정을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="be5c7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="be5c7-109">EXAMPLES</span></span>

### <span data-ttu-id="be5c7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="be5c7-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="be5c7-111">이 명령은 ' NamingService ' 섹션에서 ' MaxFileOperationTimeout '을 ' 5000 ' 값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="be5c7-112">변수</span><span class="sxs-lookup"><span data-stu-id="be5c7-112">PARAMETERS</span></span>

### <span data-ttu-id="be5c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5c7-113">-DefaultProfile</span></span>
<span data-ttu-id="be5c7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be5c7-115">-이름</span><span class="sxs-lookup"><span data-stu-id="be5c7-115">-Name</span></span>
<span data-ttu-id="be5c7-116">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="be5c7-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="be5c7-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="be5c7-117">-Parameter</span></span>
<span data-ttu-id="be5c7-118">패브릭 설정의 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="be5c7-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="be5c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="be5c7-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="be5c7-121">-섹션</span><span class="sxs-lookup"><span data-stu-id="be5c7-121">-Section</span></span>
<span data-ttu-id="be5c7-122">패브릭 설정의 섹션 이름</span><span class="sxs-lookup"><span data-stu-id="be5c7-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="be5c7-123">-Settings섹션 설명</span><span class="sxs-lookup"><span data-stu-id="be5c7-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="be5c7-124">패브릭 설정의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="be5c7-125">-값</span><span class="sxs-lookup"><span data-stu-id="be5c7-125">-Value</span></span>
<span data-ttu-id="be5c7-126">패브릭 설정의 매개 변수 값</span><span class="sxs-lookup"><span data-stu-id="be5c7-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="be5c7-127">-확인</span><span class="sxs-lookup"><span data-stu-id="be5c7-127">-Confirm</span></span>
<span data-ttu-id="be5c7-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be5c7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be5c7-129">-WhatIf</span></span>
<span data-ttu-id="be5c7-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be5c7-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be5c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5c7-132">CommonParameters</span></span>
<span data-ttu-id="be5c7-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be5c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5c7-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be5c7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5c7-135">입력</span><span class="sxs-lookup"><span data-stu-id="be5c7-135">INPUTS</span></span>

### <span data-ttu-id="be5c7-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be5c7-136">System.String</span></span>

### <span data-ttu-id="be5c7-137">ServiceFabric. Pssettings섹션 설명 []</span><span class="sxs-lookup"><span data-stu-id="be5c7-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="be5c7-138">출력</span><span class="sxs-lookup"><span data-stu-id="be5c7-138">OUTPUTS</span></span>

### <span data-ttu-id="be5c7-139">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="be5c7-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="be5c7-140">상속자</span><span class="sxs-lookup"><span data-stu-id="be5c7-140">NOTES</span></span>

## <span data-ttu-id="be5c7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be5c7-141">RELATED LINKS</span></span>
