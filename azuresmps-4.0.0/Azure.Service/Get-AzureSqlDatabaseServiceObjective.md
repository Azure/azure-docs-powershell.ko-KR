---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045568"
---
# <span data-ttu-id="f6be4-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="f6be4-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="f6be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6be4-102">SYNOPSIS</span></span>
<span data-ttu-id="f6be4-103">Azure SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="f6be4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6be4-104">SYNTAX</span></span>

### <span data-ttu-id="f6be4-105">ByConnectionContext (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6be4-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6be4-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="f6be4-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6be4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f6be4-107">DESCRIPTION</span></span>
<span data-ttu-id="f6be4-108">**AzureSqlDatabaseServiceObjective** Cmdlet은 Azure SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="f6be4-109">서비스 목표는 성능 수준 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="f6be4-110">서비스 목표를 지정 하지 않으면이 cmdlet은 지정 된 서버에 대 한 유효한 서비스 목표를 모두 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="f6be4-111">이 cmdlet은 기본, 표준 및 프리미엄 서비스 계층에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="f6be4-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f6be4-112">EXAMPLES</span></span>

### <span data-ttu-id="f6be4-113">예제 1: 연결 컨텍스트를 사용 하 여 모든 서비스 목표 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6be4-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="f6be4-114">이 명령은 연결 컨텍스트에서 $Context 지정 하는 서버의 모든 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="f6be4-115">예제 2: 서버 이름을 사용 하 여 모든 서비스 목표 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6be4-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="f6be4-116">이 명령은 Server01 이라는 서버에 대 한 모든 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="f6be4-117">변수</span><span class="sxs-lookup"><span data-stu-id="f6be4-117">PARAMETERS</span></span>

### <span data-ttu-id="f6be4-118">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f6be4-118">-Context</span></span>
<span data-ttu-id="f6be4-119">서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6be4-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="f6be4-120">-Profile</span></span>
<span data-ttu-id="f6be4-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f6be4-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6be4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6be4-123">-ServerName</span></span>
<span data-ttu-id="f6be4-124">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-124">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6be4-125">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="f6be4-125">-ServiceObjective</span></span>
<span data-ttu-id="f6be4-126">이 cmdlet이 가져오는 서비스 목표를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="f6be4-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-127">Valid values are:</span></span> 

- <span data-ttu-id="f6be4-128">기본: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="f6be4-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="f6be4-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="f6be4-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="f6be4-130">표준 (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="f6be4-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="f6be4-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="f6be4-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="f6be4-132">\* Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="f6be4-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="f6be4-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="f6be4-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="f6be4-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="f6be4-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="f6be4-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="f6be4-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="f6be4-136">프리미엄 (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="f6be4-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="f6be4-137">\* 표준 (S3)은 최신 SQL Database 업데이트 V12 (preview)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="f6be4-138">자세한 내용은 Azure library의 [AZURE SQL Database V12 Preview ()에 있는 새로운 기능](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) 을 참조 하세요 `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` .</span><span class="sxs-lookup"><span data-stu-id="f6be4-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6be4-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f6be4-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="f6be4-140">가져올 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="f6be4-141">유효한 값은 Basic, S0, S1, S2, S3, P1, P2, P3입니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6be4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6be4-142">CommonParameters</span></span>
<span data-ttu-id="f6be4-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6be4-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6be4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6be4-145">입력</span><span class="sxs-lookup"><span data-stu-id="f6be4-145">INPUTS</span></span>

### <span data-ttu-id="f6be4-146">WindowsAzure. SqlDatabase의 목표입니다.</span><span class="sxs-lookup"><span data-stu-id="f6be4-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="f6be4-147">출력</span><span class="sxs-lookup"><span data-stu-id="f6be4-147">OUTPUTS</span></span>

### <span data-ttu-id="f6be4-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="f6be4-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="f6be4-149">상속자</span><span class="sxs-lookup"><span data-stu-id="f6be4-149">NOTES</span></span>

## <span data-ttu-id="f6be4-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6be4-150">RELATED LINKS</span></span>

[<span data-ttu-id="f6be4-151">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f6be4-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="f6be4-152">서비스 수준 목표 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6be4-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="f6be4-153">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="f6be4-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f6be4-154">새로운 AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f6be4-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


