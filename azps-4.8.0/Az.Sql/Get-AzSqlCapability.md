---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213270"
---
# <span data-ttu-id="fc219-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="fc219-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="fc219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc219-102">SYNOPSIS</span></span>
<span data-ttu-id="fc219-103">현재 구독에 대 한 SQL 데이터베이스 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="fc219-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc219-104">SYNTAX</span></span>

### <span data-ttu-id="fc219-105">FilterResults (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc219-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc219-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="fc219-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc219-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc219-107">DESCRIPTION</span></span>
<span data-ttu-id="fc219-108">**AzSqlCapability** cmdlet은 지역에 대 한 현재 구독에서 사용할 수 있는 Azure SQL 데이터베이스 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="fc219-109">*Serverversionname* , *EditionName* 또는 *ServiceObjectiveName* 매개 변수를 지정 하면이 cmdlet은 지정 된 값과 해당 선행 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="fc219-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fc219-110">EXAMPLES</span></span>

### <span data-ttu-id="fc219-111">예제 1: 지역에 대 한 현재 구독에 대 한 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc219-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="fc219-112">이 명령은 중앙 US 지역에 대 한 현재 구독에서 SQL 데이터베이스 인스턴스의 기능을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="fc219-113">예제 2: 지역에 대 한 현재 구독에 대 한 기본 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc219-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="fc219-114">이 명령은 중앙 US 영역의 현재 구독에 대 한 SQL 데이터베이스의 기본 기능을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="fc219-115">예제 3: 서비스 목표에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc219-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="fc219-116">이 명령은 현재 구독에서 지정 된 서비스 목표에 대 한 SQL 데이터베이스의 기본 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="fc219-117">변수</span><span class="sxs-lookup"><span data-stu-id="fc219-117">PARAMETERS</span></span>

### <span data-ttu-id="fc219-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc219-118">-DefaultProfile</span></span>
<span data-ttu-id="fc219-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc219-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc219-120">-기본값</span><span class="sxs-lookup"><span data-stu-id="fc219-120">-Defaults</span></span>
<span data-ttu-id="fc219-121">이 cmdlet이 기본값으로만 지정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc219-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="fc219-122">-EditionName</span></span>
<span data-ttu-id="fc219-123">이 cmdlet이 기능을 가져오는 데이터베이스 버전의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc219-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="fc219-124">-LocationName</span></span>
<span data-ttu-id="fc219-125">이 cmdlet이 기능을 가져오는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="fc219-126">자세한 내용은 Azure 지역 ()을 참조 하세요 http://azure.microsoft.com/en-us/regions/ http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="fc219-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="fc219-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="fc219-127">-ServerVersionName</span></span>
<span data-ttu-id="fc219-128">이 cmdlet이 기능을 가져오는 서버 버전의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc219-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="fc219-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="fc219-130">이 cmdlet이 기능을 가져오는 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc219-131">-확인</span><span class="sxs-lookup"><span data-stu-id="fc219-131">-Confirm</span></span>
<span data-ttu-id="fc219-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc219-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc219-133">-WhatIf</span></span>
<span data-ttu-id="fc219-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc219-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc219-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc219-136">CommonParameters</span></span>
<span data-ttu-id="fc219-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc219-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc219-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc219-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc219-139">입력</span><span class="sxs-lookup"><span data-stu-id="fc219-139">INPUTS</span></span>

### <span data-ttu-id="fc219-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc219-140">System.String</span></span>

## <span data-ttu-id="fc219-141">출력</span><span class="sxs-lookup"><span data-stu-id="fc219-141">OUTPUTS</span></span>

### <span data-ttu-id="fc219-142">Microsoft.Azure.Commands.Sql.Location_Capabilities LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="fc219-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="fc219-143">상속자</span><span class="sxs-lookup"><span data-stu-id="fc219-143">NOTES</span></span>

## <span data-ttu-id="fc219-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc219-144">RELATED LINKS</span></span>
