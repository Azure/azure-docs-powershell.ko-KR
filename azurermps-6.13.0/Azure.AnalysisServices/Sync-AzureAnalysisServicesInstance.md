---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526460"
---
# <span data-ttu-id="25a8e-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="25a8e-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="25a8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a8e-102">SYNOPSIS</span></span>

<span data-ttu-id="25a8e-103">지정 된 Analysis Services 서버 인스턴스에서 지정 된 데이터베이스를 Add-AzureAnalysisServicesAccount 명령에 지정 된 현재 로그인 된 환경의 모든 query scaleout instance로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25a8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25a8e-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25a8e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25a8e-105">DESCRIPTION</span></span>

<span data-ttu-id="25a8e-106">Sync-AzureAnalysisServicesInstance cmdlet은 지정 된 Analysis Services server 인스턴스의 지정 된 데이터베이스를 Add-AzureAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경의 모든 query scaleout instance로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="25a8e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="25a8e-107">EXAMPLES</span></span>

### <span data-ttu-id="25a8e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="25a8e-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="25a8e-109">이 명령은 사용자가 Add-AzureAnalysisServicesAccount 명령을 사용 하 여이 환경에 로그인 한 환경에서 ' contoso ' 라는 서버의 SalesOrders 데이터베이스를 동기화 합니다. westus.asazure.windows.net를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="25a8e-110">변수</span><span class="sxs-lookup"><span data-stu-id="25a8e-110">PARAMETERS</span></span>

### <span data-ttu-id="25a8e-111">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="25a8e-111">-Database</span></span>

<span data-ttu-id="25a8e-112">동기화 할 데이터베이스의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="25a8e-113">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="25a8e-113">-Instance</span></span>

<span data-ttu-id="25a8e-114">다시 시작할 Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="25a8e-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="25a8e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25a8e-115">-PassThru</span></span>

<span data-ttu-id="25a8e-116">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="25a8e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="25a8e-117">-Confirm</span></span>
<span data-ttu-id="25a8e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a8e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a8e-119">-WhatIf</span></span>
<span data-ttu-id="25a8e-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25a8e-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a8e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a8e-122">CommonParameters</span></span>
<span data-ttu-id="25a8e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a8e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a8e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a8e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a8e-125">입력</span><span class="sxs-lookup"><span data-stu-id="25a8e-125">INPUTS</span></span>

### <span data-ttu-id="25a8e-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="25a8e-126">System.String</span></span>
<span data-ttu-id="25a8e-127">매개 변수: Database (ByValue), Instance (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25a8e-127">Parameters: Database (ByValue), Instance (ByValue)</span></span>

## <span data-ttu-id="25a8e-128">출력</span><span class="sxs-lookup"><span data-stu-id="25a8e-128">OUTPUTS</span></span>

### <span data-ttu-id="25a8e-129">AnalysisServices. ScaleOutServerDatabaseSyncDetails에 대 한.</span><span class="sxs-lookup"><span data-stu-id="25a8e-129">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="25a8e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="25a8e-130">NOTES</span></span>

<span data-ttu-id="25a8e-131">별칭: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="25a8e-131">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="25a8e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25a8e-132">RELATED LINKS</span></span>
