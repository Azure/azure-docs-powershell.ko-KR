---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959227"
---
# <span data-ttu-id="d1e48-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="d1e48-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="d1e48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1e48-102">SYNOPSIS</span></span>

<span data-ttu-id="d1e48-103">Analysis Services 서버의 지정된 인스턴스에서 지정된 데이터베이스를 현재 로그온된 환경의 모든 쿼리 확장 인스턴스에 동기화하는 Add-AzAnalysisServicesAccount 명령</span><span class="sxs-lookup"><span data-stu-id="d1e48-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d1e48-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1e48-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1e48-105">설명</span><span class="sxs-lookup"><span data-stu-id="d1e48-105">DESCRIPTION</span></span>

<span data-ttu-id="d1e48-106">Sync-AzAnalysisServicesInstance cmdlet은 Analysis Add-AzAnalysisServicesAccount Services 서버의 지정된 데이터베이스를 현재 로그온된 환경의 모든 쿼리 확장 인스턴스와 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e48-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d1e48-107">예제</span><span class="sxs-lookup"><span data-stu-id="d1e48-107">EXAMPLES</span></span>

### <span data-ttu-id="d1e48-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1e48-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="d1e48-109">이 명령은 사용자가 이 환경에 로그인한 경우 환경에서 'contoso'라는 서버의 SalesOrders라는 데이터베이스를 westus.asazure.windows.net 명령을 사용하여 이 환경에 Add-AzAnalysisServicesAccount 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e48-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="d1e48-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e48-110">PARAMETERS</span></span>

### <span data-ttu-id="d1e48-111">-Database</span><span class="sxs-lookup"><span data-stu-id="d1e48-111">-Database</span></span>

<span data-ttu-id="d1e48-112">동기화할 데이터베이스의 ID</span><span class="sxs-lookup"><span data-stu-id="d1e48-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e48-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="d1e48-113">-Instance</span></span>

<span data-ttu-id="d1e48-114">다시 시작할 Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="d1e48-114">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e48-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1e48-115">-PassThru</span></span>

<span data-ttu-id="d1e48-116">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e48-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d1e48-117">-확인</span><span class="sxs-lookup"><span data-stu-id="d1e48-117">-Confirm</span></span>
<span data-ttu-id="d1e48-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e48-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e48-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e48-119">-WhatIf</span></span>
<span data-ttu-id="d1e48-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1e48-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1e48-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1e48-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e48-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e48-122">CommonParameters</span></span>
<span data-ttu-id="d1e48-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e48-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e48-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1e48-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e48-125">입력</span><span class="sxs-lookup"><span data-stu-id="d1e48-125">INPUTS</span></span>

### <span data-ttu-id="d1e48-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d1e48-126">System.String</span></span>

## <span data-ttu-id="d1e48-127">출력</span><span class="sxs-lookup"><span data-stu-id="d1e48-127">OUTPUTS</span></span>

### <span data-ttu-id="d1e48-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="d1e48-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="d1e48-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1e48-129">NOTES</span></span>

<span data-ttu-id="d1e48-130">별칭: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="d1e48-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="d1e48-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1e48-131">RELATED LINKS</span></span>
