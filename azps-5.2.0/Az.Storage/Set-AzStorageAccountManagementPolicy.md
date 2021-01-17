---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b52dc34ddffb2234962888407ed67c487f4195c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348302"
---
# <span data-ttu-id="6f318-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6f318-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="6f318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f318-102">SYNOPSIS</span></span>
<span data-ttu-id="6f318-103">Azure Storage 계정의 관리 정책을 만들거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="6f318-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f318-104">SYNTAX</span></span>

### <span data-ttu-id="6f318-105">AccountNamePolicyRule(기본값)</span><span class="sxs-lookup"><span data-stu-id="6f318-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f318-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="6f318-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f318-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6f318-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f318-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6f318-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f318-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6f318-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f318-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6f318-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f318-111">설명</span><span class="sxs-lookup"><span data-stu-id="6f318-111">DESCRIPTION</span></span>
<span data-ttu-id="6f318-112">**Set-AzStorageAccountManagementPolicy** cmdlet은 Azure Storage 계정의 관리 정책을 만들거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="6f318-113">예제</span><span class="sxs-lookup"><span data-stu-id="6f318-113">EXAMPLES</span></span>

### <span data-ttu-id="6f318-114">예제 1: ManagementPolicy 규칙 개체를 사용하여 Storage 계정의 관리 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="6f318-115">이 명령은 먼저 2 ManagementPolicy 규칙 개체를 만든 다음 2 ManagementPolicy 규칙 개체를 사용하여 Storage 계정의 관리 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="6f318-116">예제 2: Json 형식 정책을 사용하여 Storage 계정의 관리 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled=$true;
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=30};
                    TierToArchive=@{DaysAfterModificationGreaterThan=50};
                    Delete=@{DaysAfterModificationGreaterThan=100};
                });
                Snapshot=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled=$false;
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=80};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  false,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="6f318-117">이 명령은 json 형식 정책을 사용하여 Storage 계정의 관리 정책을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="6f318-118">예제 3: Storage 계정에서 관리 정책을 다가 다른 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="6f318-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="6f318-119">이 명령은 먼저 Storage 계정에서 관리 정책을인 다음, 다른 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="6f318-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f318-120">PARAMETERS</span></span>

### <span data-ttu-id="6f318-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f318-121">-DefaultProfile</span></span>
<span data-ttu-id="6f318-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f318-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="6f318-123">-Policy</span></span>
<span data-ttu-id="6f318-124">설정할 관리 정책 개체</span><span class="sxs-lookup"><span data-stu-id="6f318-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f318-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f318-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f318-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f318-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="6f318-127">-Rule</span></span>
<span data-ttu-id="6f318-128">관리 정책 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-128">The Management Policy rules.</span></span> <span data-ttu-id="6f318-129">cmdlet을 New-AzStorageAccountManagementPolicyRule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f318-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f318-130">-StorageAccount</span></span>
<span data-ttu-id="6f318-131">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="6f318-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f318-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f318-132">-StorageAccountName</span></span>
<span data-ttu-id="6f318-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f318-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6f318-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="6f318-135">Storage 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f318-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f318-136">-Confirm</span></span>
<span data-ttu-id="6f318-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f318-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f318-138">-WhatIf</span></span>
<span data-ttu-id="6f318-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6f318-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f318-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f318-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f318-141">CommonParameters</span></span>
<span data-ttu-id="6f318-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f318-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f318-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f318-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f318-144">입력</span><span class="sxs-lookup"><span data-stu-id="6f318-144">INPUTS</span></span>

### <span data-ttu-id="6f318-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6f318-145">System.String</span></span>

## <span data-ttu-id="6f318-146">출력</span><span class="sxs-lookup"><span data-stu-id="6f318-146">OUTPUTS</span></span>

### <span data-ttu-id="6f318-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6f318-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="6f318-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f318-148">NOTES</span></span>

## <span data-ttu-id="6f318-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f318-149">RELATED LINKS</span></span>
