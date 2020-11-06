---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534183"
---
# <span data-ttu-id="b0bf9-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b0bf9-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="b0bf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bf9-103">Azure SQL 데이터베이스 관리 인스턴스의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0bf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0bf9-104">SYNTAX</span></span>

### <span data-ttu-id="b0bf9-105">SetInstanceFromInputParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="b0bf9-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0bf9-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b0bf9-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0bf9-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="b0bf9-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0bf9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b0bf9-108">DESCRIPTION</span></span>
<span data-ttu-id="b0bf9-109">**AzureRmSqlInstance** Cmdlet은 Azure SQL Database 관리 인스턴스의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="b0bf9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b0bf9-110">EXAMPLES</span></span>

### <span data-ttu-id="b0bf9-111">예제 1:-관리자 암호,-LicenseType,-StorageSizeInGB 및-VCore에 대 한 새 값을 사용 하 여 기존 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="b0bf9-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
```

<span data-ttu-id="b0bf9-112">이 명령은-관리자 암호,-LicenseType,-StorageSizeInGB 및-VCore에 대 한 새 값을 사용 하 여 기존 인스턴스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="b0bf9-113">변수</span><span class="sxs-lookup"><span data-stu-id="b0bf9-113">PARAMETERS</span></span>

### <span data-ttu-id="b0bf9-114">-관리자 암호</span><span class="sxs-lookup"><span data-stu-id="b0bf9-114">-AdministratorPassword</span></span>
<span data-ttu-id="b0bf9-115">인스턴스에 대 한 새 SQL 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-116">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="b0bf9-116">-AssignIdentity</span></span>
<span data-ttu-id="b0bf9-117">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 인스턴스에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="b0bf9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bf9-118">-DefaultProfile</span></span>
<span data-ttu-id="b0bf9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0bf9-120">-에디션</span><span class="sxs-lookup"><span data-stu-id="b0bf9-120">-Edition</span></span>
<span data-ttu-id="b0bf9-121">인스턴스에 할당할 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-121">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="b0bf9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b0bf9-122">-Force</span></span>
<span data-ttu-id="b0bf9-123">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="b0bf9-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b0bf9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0bf9-124">-InputObject</span></span>
<span data-ttu-id="b0bf9-125">제거할 AzureSqlManagedInstanceModel 개체</span><span class="sxs-lookup"><span data-stu-id="b0bf9-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b0bf9-126">-LicenseType</span></span>
<span data-ttu-id="b0bf9-127">사용할 인스턴스의 라이선스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-127">Determines which License Type of instance to use</span></span>

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

### <span data-ttu-id="b0bf9-128">-이름</span><span class="sxs-lookup"><span data-stu-id="b0bf9-128">-Name</span></span>
<span data-ttu-id="b0bf9-129">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0bf9-130">-ResourceGroupName</span></span>
<span data-ttu-id="b0bf9-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0bf9-132">-ResourceId</span></span>
<span data-ttu-id="b0bf9-133">제거할 인스턴스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b0bf9-134">-StorageSizeInGB</span></span>
<span data-ttu-id="b0bf9-135">인스턴스와 연결할 저장소 크기의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-136">태그</span><span class="sxs-lookup"><span data-stu-id="b0bf9-136">-Tag</span></span>
<span data-ttu-id="b0bf9-137">인스턴스와 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-137">The tags to associate with the instance.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="b0bf9-138">-VCore</span></span>
<span data-ttu-id="b0bf9-139">인스턴스와 연결할 VCore의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-140">-확인</span><span class="sxs-lookup"><span data-stu-id="b0bf9-140">-Confirm</span></span>
<span data-ttu-id="b0bf9-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0bf9-142">-WhatIf</span></span>
<span data-ttu-id="b0bf9-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0bf9-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bf9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bf9-145">CommonParameters</span></span>
<span data-ttu-id="b0bf9-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bf9-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0bf9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bf9-148">입력</span><span class="sxs-lookup"><span data-stu-id="b0bf9-148">INPUTS</span></span>

### <span data-ttu-id="b0bf9-149">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="b0bf9-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="b0bf9-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0bf9-150">System.String</span></span>

## <span data-ttu-id="b0bf9-151">출력</span><span class="sxs-lookup"><span data-stu-id="b0bf9-151">OUTPUTS</span></span>

### <span data-ttu-id="b0bf9-152">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="b0bf9-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="b0bf9-153">상속자</span><span class="sxs-lookup"><span data-stu-id="b0bf9-153">NOTES</span></span>

## <span data-ttu-id="b0bf9-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0bf9-154">RELATED LINKS</span></span>
