---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 44f5ffd63f2bb89f2e26d8ded6a0c7f64181bf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711691"
---
# <span data-ttu-id="0c8bc-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="0c8bc-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="0c8bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8bc-103">컴퓨터에서 IIS 로그 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c8bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c8bc-104">SYNTAX</span></span>

### <span data-ttu-id="0c8bc-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c8bc-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c8bc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0c8bc-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c8bc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0c8bc-107">DESCRIPTION</span></span>
<span data-ttu-id="0c8bc-108">**AzureRmOperationalInsightsIISLogCollection** cmdlet은 작업 영역에 연결 된 컴퓨터의 IIS (인터넷 정보 서비스) 로그 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="0c8bc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c8bc-109">EXAMPLES</span></span>

## <span data-ttu-id="0c8bc-110">변수</span><span class="sxs-lookup"><span data-stu-id="0c8bc-110">PARAMETERS</span></span>

### <span data-ttu-id="0c8bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8bc-111">-DefaultProfile</span></span>
<span data-ttu-id="0c8bc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c8bc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c8bc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c8bc-113">-ResourceGroupName</span></span>
<span data-ttu-id="0c8bc-114">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c8bc-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="0c8bc-115">-Workspace</span></span>
<span data-ttu-id="0c8bc-116">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c8bc-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c8bc-117">-WorkspaceName</span></span>
<span data-ttu-id="0c8bc-118">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c8bc-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0c8bc-119">-Confirm</span></span>
<span data-ttu-id="0c8bc-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c8bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c8bc-121">-WhatIf</span></span>
<span data-ttu-id="0c8bc-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c8bc-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c8bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8bc-124">CommonParameters</span></span>
<span data-ttu-id="0c8bc-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8bc-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c8bc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8bc-127">입력</span><span class="sxs-lookup"><span data-stu-id="0c8bc-127">INPUTS</span></span>

### <span data-ttu-id="0c8bc-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c8bc-128">PSWorkspace</span></span>
<span data-ttu-id="0c8bc-129">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0c8bc-130">출력</span><span class="sxs-lookup"><span data-stu-id="0c8bc-130">OUTPUTS</span></span>

### <span data-ttu-id="0c8bc-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0c8bc-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0c8bc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="0c8bc-132">NOTES</span></span>
* <span data-ttu-id="0c8bc-133">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="0c8bc-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0c8bc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c8bc-134">RELATED LINKS</span></span>

[<span data-ttu-id="0c8bc-135">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="0c8bc-135">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


