---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: cc91184374575b25f34669d7e22c80b620d34ced
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976171"
---
# <span data-ttu-id="386c0-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="386c0-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="386c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="386c0-102">SYNOPSIS</span></span>
<span data-ttu-id="386c0-103">Azure Storage 계정의 관리 정책을 만들거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="386c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="386c0-104">SYNTAX</span></span>

### <span data-ttu-id="386c0-105">AccountNamePolicyRule(기본값)</span><span class="sxs-lookup"><span data-stu-id="386c0-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="386c0-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="386c0-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="386c0-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="386c0-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="386c0-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="386c0-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="386c0-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="386c0-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="386c0-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="386c0-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="386c0-111">설명</span><span class="sxs-lookup"><span data-stu-id="386c0-111">DESCRIPTION</span></span>
<span data-ttu-id="386c0-112">**Set-AzStorageAccountManagementPolicy** cmdlet은 Azure Storage 계정의 관리 정책을 만들거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="386c0-113">예제</span><span class="sxs-lookup"><span data-stu-id="386c0-113">EXAMPLES</span></span>

### <span data-ttu-id="386c0-114">예제 1: ManagementPolicy 규칙 개체를 사용하여 Storage 계정의 관리 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -InputObject $action2 -BlobVersionAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter -BlobType appendBlob,blockBlob
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 2/19/2021 10:13:00 AM
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
                                                                                            },
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null
                                                                             },
                                                                "Version":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "ab",
                                                                                    "cd"
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
                                                                "BaseBlob":  null,
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            },
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null
                                                                             },
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  null,
                                                                                "TierToArchive":  null
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "appendBlob",
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="386c0-115">이 명령은 먼저 2 ManagementPolicy 규칙 개체를 만든 다음, 2 ManagementPolicy 규칙 개체로 Storage 계정의 관리 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="386c0-116">예제 2: Json 형식 정책을 사용하여 Storage 계정의 관리 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
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
                    TierToArchive=@{DaysAfterCreationGreaterThan=50};
                    TierToCool=@{DaysAfterCreationGreaterThan=60};
                });
                Version=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                    TierToArchive=@{DaysAfterCreationGreaterThan=50};
                    TierToCool=@{DaysAfterCreationGreaterThan=60};
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
                Version=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob","appendBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 2/19/2021 10:16:32 AM
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
                                                                                            },
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterCreationGreaterThan":  60
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterCreationGreaterThan":  50
                                                                                                   }
                                                                             },
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  {
                                                                                                   "DaysAfterCreationGreaterThan":  60
                                                                                               },
                                                                                "TierToArchive":  {
                                                                                                      "DaysAfterCreationGreaterThan":  50
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
                                                                "BaseBlob":  null,
                                                                "Snapshot":  null,
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  null,
                                                                                "TierToArchive":  null
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob",
                                                                                  "appendBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="386c0-117">이 명령은 json 형식 정책을 사용하여 Storage 계정의 관리 정책을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="386c0-118">예제 3: Storage 계정에서 관리 정책을 한 다음 다른 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="386c0-119">이 명령은 먼저 Storage 계정에서 관리 정책을 얻은 다음 다른 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="386c0-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="386c0-120">PARAMETERS</span></span>

### <span data-ttu-id="386c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386c0-121">-DefaultProfile</span></span>
<span data-ttu-id="386c0-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="386c0-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="386c0-123">-Policy</span></span>
<span data-ttu-id="386c0-124">설정할 관리 정책 개체</span><span class="sxs-lookup"><span data-stu-id="386c0-124">Management Policy Object to Set</span></span>

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

### <span data-ttu-id="386c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="386c0-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="386c0-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="386c0-127">-Rule</span></span>
<span data-ttu-id="386c0-128">관리 정책 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-128">The Management Policy rules.</span></span> <span data-ttu-id="386c0-129">cmdlet을 New-AzStorageAccountManagementPolicyRule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

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

### <span data-ttu-id="386c0-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="386c0-130">-StorageAccount</span></span>
<span data-ttu-id="386c0-131">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="386c0-131">Storage account object</span></span>

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

### <span data-ttu-id="386c0-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="386c0-132">-StorageAccountName</span></span>
<span data-ttu-id="386c0-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="386c0-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="386c0-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="386c0-135">Storage 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-135">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="386c0-136">-확인</span><span class="sxs-lookup"><span data-stu-id="386c0-136">-Confirm</span></span>
<span data-ttu-id="386c0-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="386c0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="386c0-138">-WhatIf</span></span>
<span data-ttu-id="386c0-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="386c0-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="386c0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386c0-141">CommonParameters</span></span>
<span data-ttu-id="386c0-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="386c0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386c0-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="386c0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386c0-144">입력</span><span class="sxs-lookup"><span data-stu-id="386c0-144">INPUTS</span></span>

### <span data-ttu-id="386c0-145">System.String</span><span class="sxs-lookup"><span data-stu-id="386c0-145">System.String</span></span>

## <span data-ttu-id="386c0-146">출력</span><span class="sxs-lookup"><span data-stu-id="386c0-146">OUTPUTS</span></span>

### <span data-ttu-id="386c0-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="386c0-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="386c0-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="386c0-148">NOTES</span></span>

## <span data-ttu-id="386c0-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="386c0-149">RELATED LINKS</span></span>
