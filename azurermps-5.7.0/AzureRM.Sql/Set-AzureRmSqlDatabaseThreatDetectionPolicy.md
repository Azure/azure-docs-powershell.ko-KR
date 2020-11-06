---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: aa70b94614f8a0826a5d1563439afa8cb9ef6d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534556"
---
# <span data-ttu-id="d0465-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0465-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="d0465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0465-102">SYNOPSIS</span></span>
<span data-ttu-id="d0465-103">데이터베이스에 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0465-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0465-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0465-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d0465-105">DESCRIPTION</span></span>
<span data-ttu-id="d0465-106">**AzureRmSqlDatabaseThreatDetectionPolicy** Cmdlet은 Azure SQL 데이터베이스에 대 한 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="d0465-107">데이터베이스에서 위협 검색을 사용 하도록 설정 하려면 해당 데이터베이스에서 감사 정책을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="d0465-108">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="d0465-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d0465-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d0465-110">EXAMPLES</span></span>

### <span data-ttu-id="d0465-111">예제 1: 데이터베이스에 대 한 위협 검색 정책 설정</span><span class="sxs-lookup"><span data-stu-id="d0465-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="d0465-112">이 명령은 Server01 라는 서버의 Database01 이라는 데이터베이스에 대 한 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="d0465-113">변수</span><span class="sxs-lookup"><span data-stu-id="d0465-113">PARAMETERS</span></span>

### <span data-ttu-id="d0465-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0465-114">-DatabaseName</span></span>
<span data-ttu-id="d0465-115">정책이 설정 된 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-115">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0465-116">-DefaultProfile</span></span>
<span data-ttu-id="d0465-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d0465-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0465-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="d0465-118">-EmailAdmins</span></span>
<span data-ttu-id="d0465-119">위협 검색 정책이 전자 메일을 사용 하 여 관리자에 게 보낼지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="d0465-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="d0465-121">정책에서 제외할 검색 유형의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="d0465-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0465-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="d0465-123">Sql_Injection</span></span> 
- <span data-ttu-id="d0465-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="d0465-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="d0465-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="d0465-125">Access_Anomaly</span></span> 
- <span data-ttu-id="d0465-126">않아야</span><span class="sxs-lookup"><span data-stu-id="d0465-126">None</span></span>

```yaml
Type: DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="d0465-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="d0465-128">정책에서 알림을 보내는 전자 메일 주소 목록 (세미콜론으로 구분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0465-129">-PassThru</span></span>
<span data-ttu-id="d0465-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0465-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0465-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0465-132">-ResourceGroupName</span></span>
<span data-ttu-id="d0465-133">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-133">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-134">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="d0465-134">-RetentionInDays</span></span>
<span data-ttu-id="d0465-135">감사 로그 보존 일 수</span><span class="sxs-lookup"><span data-stu-id="d0465-135">The number of retention days for the audit logs</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0465-136">-ServerName</span></span>
<span data-ttu-id="d0465-137">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-137">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d0465-138">-StorageAccountName</span></span>
<span data-ttu-id="d0465-139">사용할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="d0465-140">와일드 카드는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-140">Wildcards are not permitted.</span></span> <span data-ttu-id="d0465-141">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-141">This parameter is not required.</span></span> <span data-ttu-id="d0465-142">이 매개 변수를 제공 하지 않으면 cmdlet에서 이전에 정의한 저장소 계정을 데이터베이스의 위협 검색 정책의 일부로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="d0465-143">데이터베이스 위협 검색 정책을 처음 정의 하는 경우이 매개 변수를 제공 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0465-144">-확인</span><span class="sxs-lookup"><span data-stu-id="d0465-144">-Confirm</span></span>
<span data-ttu-id="d0465-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0465-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0465-146">-WhatIf</span></span>
<span data-ttu-id="d0465-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0465-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0465-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0465-149">CommonParameters</span></span>
<span data-ttu-id="d0465-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0465-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0465-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0465-152">입력</span><span class="sxs-lookup"><span data-stu-id="d0465-152">INPUTS</span></span>

###  
<span data-ttu-id="d0465-153">이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="d0465-154">출력</span><span class="sxs-lookup"><span data-stu-id="d0465-154">OUTPUTS</span></span>

### <span data-ttu-id="d0465-155">ThreatDetection. DatabaseThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d0465-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="d0465-156">이 cmdlet은 **DatabaseThreatDetectionPolicyModel** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0465-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="d0465-157">상속자</span><span class="sxs-lookup"><span data-stu-id="d0465-157">NOTES</span></span>

## <span data-ttu-id="d0465-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0465-158">RELATED LINKS</span></span>

[<span data-ttu-id="d0465-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0465-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="d0465-160">제거-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0465-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="d0465-161">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d0465-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


