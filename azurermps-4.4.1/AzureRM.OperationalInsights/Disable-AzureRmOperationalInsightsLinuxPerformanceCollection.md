---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 0af85097efb1b8383caf41d9f5bb5328957585fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710973"
---
# <span data-ttu-id="09d34-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="09d34-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="09d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d34-102">SYNOPSIS</span></span>
<span data-ttu-id="09d34-103">Linux 컴퓨터에서 성능 카운터 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-103">Stops collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09d34-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09d34-104">SYNTAX</span></span>

### <span data-ttu-id="09d34-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="09d34-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d34-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09d34-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d34-107">설명은</span><span class="sxs-lookup"><span data-stu-id="09d34-107">DESCRIPTION</span></span>
<span data-ttu-id="09d34-108">**AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet은 작업 영역에서 연결 된 Linux 컴퓨터의 성능 카운터 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-108">The **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="09d34-109">예제의</span><span class="sxs-lookup"><span data-stu-id="09d34-109">EXAMPLES</span></span>

## <span data-ttu-id="09d34-110">변수</span><span class="sxs-lookup"><span data-stu-id="09d34-110">PARAMETERS</span></span>

### <span data-ttu-id="09d34-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d34-111">-ResourceGroupName</span></span>
<span data-ttu-id="09d34-112">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-112">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d34-113">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="09d34-113">-Workspace</span></span>
<span data-ttu-id="09d34-114">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d34-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09d34-115">-WorkspaceName</span></span>
<span data-ttu-id="09d34-116">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d34-117">-확인</span><span class="sxs-lookup"><span data-stu-id="09d34-117">-Confirm</span></span>
<span data-ttu-id="09d34-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d34-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d34-119">-WhatIf</span></span>
<span data-ttu-id="09d34-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09d34-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d34-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d34-122">-DefaultProfile</span></span>
<span data-ttu-id="09d34-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d34-124">CommonParameters</span></span>
<span data-ttu-id="09d34-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d34-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d34-127">입력</span><span class="sxs-lookup"><span data-stu-id="09d34-127">INPUTS</span></span>

### <span data-ttu-id="09d34-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="09d34-128">PSWorkspace</span></span>
<span data-ttu-id="09d34-129">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d34-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="09d34-130">출력</span><span class="sxs-lookup"><span data-stu-id="09d34-130">OUTPUTS</span></span>

### <span data-ttu-id="09d34-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="09d34-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="09d34-132">상속자</span><span class="sxs-lookup"><span data-stu-id="09d34-132">NOTES</span></span>
* <span data-ttu-id="09d34-133">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="09d34-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="09d34-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09d34-134">RELATED LINKS</span></span>

[<span data-ttu-id="09d34-135">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="09d34-135">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="09d34-136">새로운 AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="09d34-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


