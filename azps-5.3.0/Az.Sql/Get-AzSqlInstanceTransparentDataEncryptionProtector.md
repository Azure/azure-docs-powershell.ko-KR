---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492326"
---
# <span data-ttu-id="d9956-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d9956-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="d9956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9956-102">SYNOPSIS</span></span>
<span data-ttu-id="d9956-103">관리되는 인스턴스에 대한 TDE(투명한 데이터 SQL 보호기)를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="d9956-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9956-104">SYNTAX</span></span>

### <span data-ttu-id="d9956-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d9956-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9956-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9956-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9956-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9956-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9956-108">설명</span><span class="sxs-lookup"><span data-stu-id="d9956-108">DESCRIPTION</span></span>
<span data-ttu-id="d9956-109">Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet은 지정된 SQL 관리되는 인스턴스에 대한 TDE 보호기입니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="d9956-110">예제</span><span class="sxs-lookup"><span data-stu-id="d9956-110">EXAMPLES</span></span>

### <span data-ttu-id="d9956-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9956-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d9956-112">이 명령은 ContosoResourceGroup이라는 리소스 그룹의 ContosoManagedInstanceName이라는 관리되는 인스턴스에 대한 TDE 보호기입니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d9956-113">예제 2: 관리되는 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="d9956-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d9956-114">이 명령은 ContosoResourceGroup이라는 리소스 그룹의 ContosoManagedInstanceName이라는 관리되는 인스턴스에 대한 TDE 보호기입니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d9956-115">예제 3: 관리되는 인스턴스 리소스 ID 사용</span><span class="sxs-lookup"><span data-stu-id="d9956-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d9956-116">이 명령은 ContosoResourceGroup이라는 리소스 그룹의 ContosoManagedInstanceName이라는 관리되는 인스턴스에 대한 TDE 보호기입니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d9956-117">예제 4: 파이핑 사용</span><span class="sxs-lookup"><span data-stu-id="d9956-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="d9956-118">이 명령은 ContosoResourceGroup이라는 리소스 그룹의 ContosoManagedInstanceName이라는 관리되는 인스턴스에 대한 TDE 보호기입니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="d9956-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9956-119">PARAMETERS</span></span>

### <span data-ttu-id="d9956-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9956-120">-DefaultProfile</span></span>
<span data-ttu-id="d9956-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9956-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="d9956-122">-Instance</span></span>
<span data-ttu-id="d9956-123">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="d9956-123">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9956-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d9956-124">-InstanceName</span></span>
<span data-ttu-id="d9956-125">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="d9956-125">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9956-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d9956-126">-InstanceResourceId</span></span>
<span data-ttu-id="d9956-127">인스턴스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d9956-127">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9956-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9956-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9956-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d9956-129">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9956-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9956-130">-Confirm</span></span>
<span data-ttu-id="d9956-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9956-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9956-132">-WhatIf</span></span>
<span data-ttu-id="d9956-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9956-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9956-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9956-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9956-135">CommonParameters</span></span>
<span data-ttu-id="d9956-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9956-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9956-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9956-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9956-138">입력</span><span class="sxs-lookup"><span data-stu-id="d9956-138">INPUTS</span></span>

### <span data-ttu-id="d9956-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d9956-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="d9956-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d9956-140">System.String</span></span>

## <span data-ttu-id="d9956-141">출력</span><span class="sxs-lookup"><span data-stu-id="d9956-141">OUTPUTS</span></span>

### <span data-ttu-id="d9956-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="d9956-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="d9956-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9956-143">NOTES</span></span>

## <span data-ttu-id="d9956-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9956-144">RELATED LINKS</span></span>
