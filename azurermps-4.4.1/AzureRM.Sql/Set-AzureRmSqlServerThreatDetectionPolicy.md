---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537799"
---
# <span data-ttu-id="a50b9-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a50b9-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="a50b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a50b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a50b9-103">서버에서 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a50b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a50b9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a50b9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a50b9-105">DESCRIPTION</span></span>
<span data-ttu-id="a50b9-106">**AzureRmSqlServerThreatDetectionPolicy** Cmdlet은 Azure SQL server에 대 한 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="a50b9-107">서버에서 위협 검색을 사용 하도록 설정 하려면 해당 서버에서 감사 정책을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="a50b9-108">이 cmdlet을 사용 하려면 서버를 식별 하는 *ResourceGroupName* 및 ServerName 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="a50b9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a50b9-109">EXAMPLES</span></span>

### <span data-ttu-id="a50b9-110">예제 1: 데이터베이스에 대 한 위협 검색 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a50b9-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="a50b9-111">이 명령은 Server01 이라는 서버에 대 한 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="a50b9-112">변수</span><span class="sxs-lookup"><span data-stu-id="a50b9-112">PARAMETERS</span></span>

### <span data-ttu-id="a50b9-113">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="a50b9-113">-EmailAdmins</span></span>
<span data-ttu-id="a50b9-114">위협 검색 정책이 전자 메일을 사용 하 여 관리자에 게 보낼지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50b9-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="a50b9-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="a50b9-116">정책에서 제외할 검색 유형의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="a50b9-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a50b9-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="a50b9-118">Sql_Injection</span></span>
- <span data-ttu-id="a50b9-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="a50b9-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="a50b9-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="a50b9-120">Access_Anomaly</span></span>
- <span data-ttu-id="a50b9-121">않아야</span><span class="sxs-lookup"><span data-stu-id="a50b9-121">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50b9-122">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="a50b9-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="a50b9-123">정책에서 알림을 보내는 전자 메일 주소 목록 (세미콜론으로 구분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50b9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a50b9-124">-PassThru</span></span>
<span data-ttu-id="a50b9-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a50b9-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a50b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a50b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="a50b9-128">서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="a50b9-129">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="a50b9-129">-RetentionInDays</span></span>
<span data-ttu-id="a50b9-130">감사 로그 보존 일 수</span><span class="sxs-lookup"><span data-stu-id="a50b9-130">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50b9-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a50b9-131">-ServerName</span></span>
<span data-ttu-id="a50b9-132">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-132">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50b9-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a50b9-133">-StorageAccountName</span></span>
<span data-ttu-id="a50b9-134">사용할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="a50b9-135">와일드 카드는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-135">Wildcards are not permitted.</span></span> <span data-ttu-id="a50b9-136">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-136">This parameter is not required.</span></span> <span data-ttu-id="a50b9-137">이 매개 변수를 제공 하지 않으면 cmdlet에서 이전에 정의한 저장소 계정을 데이터베이스의 위협 검색 정책의 일부로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="a50b9-138">검색 정책을 정의 하는 첫 번째 데이터베이스인 경우이 매개 변수를 제공 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50b9-139">-확인</span><span class="sxs-lookup"><span data-stu-id="a50b9-139">-Confirm</span></span>
<span data-ttu-id="a50b9-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a50b9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a50b9-141">-WhatIf</span></span>
<span data-ttu-id="a50b9-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a50b9-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a50b9-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a50b9-144">-DefaultProfile</span></span>
<span data-ttu-id="a50b9-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a50b9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a50b9-146">CommonParameters</span></span>
<span data-ttu-id="a50b9-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a50b9-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a50b9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a50b9-149">입력</span><span class="sxs-lookup"><span data-stu-id="a50b9-149">INPUTS</span></span>

###  
<span data-ttu-id="a50b9-150">이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="a50b9-151">출력</span><span class="sxs-lookup"><span data-stu-id="a50b9-151">OUTPUTS</span></span>

### <span data-ttu-id="a50b9-152">ThreatDetection. ServerThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a50b9-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="a50b9-153">이 cmdlet은 **ServerThreatDetectionPolicyModel** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50b9-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="a50b9-154">상속자</span><span class="sxs-lookup"><span data-stu-id="a50b9-154">NOTES</span></span>

## <span data-ttu-id="a50b9-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a50b9-155">RELATED LINKS</span></span>

[<span data-ttu-id="a50b9-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a50b9-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="a50b9-157">제거-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a50b9-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="a50b9-158">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a50b9-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
