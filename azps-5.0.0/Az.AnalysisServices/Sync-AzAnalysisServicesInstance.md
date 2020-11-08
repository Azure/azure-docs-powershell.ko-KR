---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216473"
---
# <span data-ttu-id="ef1f1-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="ef1f1-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="ef1f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef1f1-102">SYNOPSIS</span></span>

<span data-ttu-id="ef1f1-103">지정 된 Analysis Services 서버 인스턴스에서 지정 된 데이터베이스를 Add-AzAnalysisServicesAccount 명령에 지정 된 현재 로그인 된 환경의 모든 query scaleout instance로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="ef1f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef1f1-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef1f1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef1f1-105">DESCRIPTION</span></span>

<span data-ttu-id="ef1f1-106">Sync-AzAnalysisServicesInstance cmdlet은 지정 된 Analysis Services server 인스턴스의 지정 된 데이터베이스를 Add-AzAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경의 모든 query scaleout instance로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="ef1f1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef1f1-107">EXAMPLES</span></span>

### <span data-ttu-id="ef1f1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef1f1-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="ef1f1-109">이 명령은 사용자가 Add-AzAnalysisServicesAccount 명령을 사용 하 여 로그인 한 환경에서 ' contoso ' 라는 서버의 SalesOrders 데이터베이스를 동기화 합니다. westus.asazure.windows.net를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="ef1f1-110">변수</span><span class="sxs-lookup"><span data-stu-id="ef1f1-110">PARAMETERS</span></span>

### <span data-ttu-id="ef1f1-111">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="ef1f1-111">-Database</span></span>

<span data-ttu-id="ef1f1-112">동기화 할 데이터베이스의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="ef1f1-113">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="ef1f1-113">-Instance</span></span>

<span data-ttu-id="ef1f1-114">다시 시작할 Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="ef1f1-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="ef1f1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef1f1-115">-PassThru</span></span>

<span data-ttu-id="ef1f1-116">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ef1f1-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ef1f1-117">-Confirm</span></span>
<span data-ttu-id="ef1f1-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1f1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1f1-119">-WhatIf</span></span>
<span data-ttu-id="ef1f1-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef1f1-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1f1-122">CommonParameters</span></span>
<span data-ttu-id="ef1f1-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1f1-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1f1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1f1-125">입력</span><span class="sxs-lookup"><span data-stu-id="ef1f1-125">INPUTS</span></span>

### <span data-ttu-id="ef1f1-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef1f1-126">System.String</span></span>

## <span data-ttu-id="ef1f1-127">출력</span><span class="sxs-lookup"><span data-stu-id="ef1f1-127">OUTPUTS</span></span>

### <span data-ttu-id="ef1f1-128">AnalysisServices. ScaleOutServerDatabaseSyncDetails에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ef1f1-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="ef1f1-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ef1f1-129">NOTES</span></span>

<span data-ttu-id="ef1f1-130">별칭: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="ef1f1-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="ef1f1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef1f1-131">RELATED LINKS</span></span>
