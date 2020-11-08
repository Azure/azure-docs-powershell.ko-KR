---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034047"
---
# <span data-ttu-id="a67dd-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a67dd-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="a67dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a67dd-103">SQL 관리 인스턴스에 대 한 TDE (투명 한 데이터 암호화) 보호기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="a67dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a67dd-104">SYNTAX</span></span>

### <span data-ttu-id="a67dd-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a67dd-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a67dd-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a67dd-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a67dd-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a67dd-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a67dd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a67dd-108">DESCRIPTION</span></span>
<span data-ttu-id="a67dd-109">Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet은 지정 된 SQL 관리 인스턴스에 대 한 TDE 프로텍터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="a67dd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a67dd-110">EXAMPLES</span></span>

### <span data-ttu-id="a67dd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a67dd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a67dd-112">이 명령은 ContosoResourceGroup 이라는 리소스 그룹의 ContosoManagedInstanceName 이라는 관리 되는 인스턴스에 대 한 TDE 프로텍터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a67dd-113">예제 2: 관리 되는 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="a67dd-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a67dd-114">이 명령은 ContosoResourceGroup 이라는 리소스 그룹의 ContosoManagedInstanceName 이라는 관리 되는 인스턴스에 대 한 TDE 프로텍터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a67dd-115">예제 3: 관리 되는 인스턴스 리소스 id 사용</span><span class="sxs-lookup"><span data-stu-id="a67dd-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a67dd-116">이 명령은 ContosoResourceGroup 이라는 리소스 그룹의 ContosoManagedInstanceName 이라는 관리 되는 인스턴스에 대 한 TDE 프로텍터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a67dd-117">예제 4: 배관 사용</span><span class="sxs-lookup"><span data-stu-id="a67dd-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="a67dd-118">이 명령은 ContosoResourceGroup 이라는 리소스 그룹의 ContosoManagedInstanceName 이라는 관리 되는 인스턴스에 대 한 TDE 프로텍터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="a67dd-119">변수</span><span class="sxs-lookup"><span data-stu-id="a67dd-119">PARAMETERS</span></span>

### <span data-ttu-id="a67dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67dd-120">-DefaultProfile</span></span>
<span data-ttu-id="a67dd-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a67dd-122">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="a67dd-122">-Instance</span></span>
<span data-ttu-id="a67dd-123">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="a67dd-123">The instance input object</span></span>

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

### <span data-ttu-id="a67dd-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a67dd-124">-InstanceName</span></span>
<span data-ttu-id="a67dd-125">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="a67dd-125">The instance name</span></span>

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

### <span data-ttu-id="a67dd-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="a67dd-126">-InstanceResourceId</span></span>
<span data-ttu-id="a67dd-127">인스턴스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a67dd-127">The instance resource id</span></span>

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

### <span data-ttu-id="a67dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="a67dd-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a67dd-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="a67dd-130">-확인</span><span class="sxs-lookup"><span data-stu-id="a67dd-130">-Confirm</span></span>
<span data-ttu-id="a67dd-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67dd-132">-WhatIf</span></span>
<span data-ttu-id="a67dd-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a67dd-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67dd-135">CommonParameters</span></span>
<span data-ttu-id="a67dd-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67dd-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a67dd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67dd-138">입력</span><span class="sxs-lookup"><span data-stu-id="a67dd-138">INPUTS</span></span>

### <span data-ttu-id="a67dd-139">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="a67dd-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="a67dd-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a67dd-140">System.String</span></span>

## <span data-ttu-id="a67dd-141">출력</span><span class="sxs-lookup"><span data-stu-id="a67dd-141">OUTPUTS</span></span>

### <span data-ttu-id="a67dd-142">TransparentDataEncryption. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a67dd-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="a67dd-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a67dd-143">NOTES</span></span>

## <span data-ttu-id="a67dd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a67dd-144">RELATED LINKS</span></span>
