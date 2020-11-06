---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 4c71a5b71c04c8593443820989c935852b8a002b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530737"
---
# <span data-ttu-id="e7443-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="e7443-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="e7443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7443-102">SYNOPSIS</span></span>
<span data-ttu-id="e7443-103">사용자 지정 로그 수집 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7443-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7443-104">SYNTAX</span></span>

### <span data-ttu-id="e7443-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7443-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7443-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e7443-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7443-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e7443-107">DESCRIPTION</span></span>
<span data-ttu-id="e7443-108">**새 AzureRmOperationalInsightsCustomLogDataSource** cmdlet은 사용자 지정 로그 수집 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="e7443-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e7443-109">EXAMPLES</span></span>

## <span data-ttu-id="e7443-110">변수</span><span class="sxs-lookup"><span data-stu-id="e7443-110">PARAMETERS</span></span>

### <span data-ttu-id="e7443-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="e7443-111">-CustomLogRawJson</span></span>
<span data-ttu-id="e7443-112">사용자 지정 컬렉션 정책을 JSON (원시 JavaScript 개체 표기) 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7443-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e7443-113">-Force</span></span>
<span data-ttu-id="e7443-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7443-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e7443-115">-Name</span></span>
<span data-ttu-id="e7443-116">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-116">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7443-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7443-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7443-118">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="e7443-119">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="e7443-119">-Workspace</span></span>
<span data-ttu-id="e7443-120">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e7443-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e7443-121">-WorkspaceName</span></span>
<span data-ttu-id="e7443-122">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e7443-123">-확인</span><span class="sxs-lookup"><span data-stu-id="e7443-123">-Confirm</span></span>
<span data-ttu-id="e7443-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7443-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7443-125">-WhatIf</span></span>
<span data-ttu-id="e7443-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7443-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7443-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7443-128">-DefaultProfile</span></span>
<span data-ttu-id="e7443-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7443-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7443-130">CommonParameters</span></span>
<span data-ttu-id="e7443-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7443-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7443-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7443-133">입력</span><span class="sxs-lookup"><span data-stu-id="e7443-133">INPUTS</span></span>

### <span data-ttu-id="e7443-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e7443-134">PSWorkspace</span></span>
<span data-ttu-id="e7443-135">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7443-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e7443-136">출력</span><span class="sxs-lookup"><span data-stu-id="e7443-136">OUTPUTS</span></span>

### <span data-ttu-id="e7443-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e7443-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e7443-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e7443-138">NOTES</span></span>

## <span data-ttu-id="e7443-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7443-139">RELATED LINKS</span></span>

[<span data-ttu-id="e7443-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e7443-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="e7443-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e7443-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

