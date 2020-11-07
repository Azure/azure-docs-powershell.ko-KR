---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: a3f650861f70ad9110f4716e5034cd5e7f930343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704161"
---
# <span data-ttu-id="5088c-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5088c-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5088c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5088c-102">SYNOPSIS</span></span>
<span data-ttu-id="5088c-103">데이터 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5088c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5088c-104">SYNTAX</span></span>

### <span data-ttu-id="5088c-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5088c-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5088c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5088c-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5088c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5088c-107">DESCRIPTION</span></span>
<span data-ttu-id="5088c-108">**제거-AzureRmOperationalInsightsDataSource** cmdlet은 데이터 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="5088c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5088c-109">EXAMPLES</span></span>

## <span data-ttu-id="5088c-110">변수</span><span class="sxs-lookup"><span data-stu-id="5088c-110">PARAMETERS</span></span>

### <span data-ttu-id="5088c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5088c-111">-DefaultProfile</span></span>
<span data-ttu-id="5088c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5088c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5088c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5088c-113">-Force</span></span>
<span data-ttu-id="5088c-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5088c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5088c-115">-Name</span></span>
<span data-ttu-id="5088c-116">삭제할 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5088c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5088c-117">-ResourceGroupName</span></span>
<span data-ttu-id="5088c-118">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5088c-119">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="5088c-119">-Workspace</span></span>
<span data-ttu-id="5088c-120">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5088c-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5088c-121">-WorkspaceName</span></span>
<span data-ttu-id="5088c-122">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5088c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5088c-123">-Confirm</span></span>
<span data-ttu-id="5088c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5088c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5088c-125">-WhatIf</span></span>
<span data-ttu-id="5088c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5088c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5088c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5088c-128">CommonParameters</span></span>
<span data-ttu-id="5088c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5088c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5088c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5088c-131">입력</span><span class="sxs-lookup"><span data-stu-id="5088c-131">INPUTS</span></span>

### <span data-ttu-id="5088c-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5088c-132">PSWorkspace</span></span>
<span data-ttu-id="5088c-133">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5088c-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="5088c-134">출력</span><span class="sxs-lookup"><span data-stu-id="5088c-134">OUTPUTS</span></span>

## <span data-ttu-id="5088c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5088c-135">NOTES</span></span>
* <span data-ttu-id="5088c-136">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="5088c-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5088c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5088c-137">RELATED LINKS</span></span>

[<span data-ttu-id="5088c-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5088c-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="5088c-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5088c-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


