---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 82faf45a348eb1e84fdc0c577c27a4d68fda3894
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204226"
---
# <span data-ttu-id="25394-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="25394-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="25394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25394-102">SYNOPSIS</span></span>
<span data-ttu-id="25394-103">Azure 저장소 계정의 관리 정책을 만들거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="25394-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25394-104">SYNTAX</span></span>

### <span data-ttu-id="25394-105">AccountNamePolicyRule (기본값)</span><span class="sxs-lookup"><span data-stu-id="25394-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25394-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="25394-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25394-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="25394-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25394-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="25394-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25394-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="25394-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25394-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="25394-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25394-111">설명은</span><span class="sxs-lookup"><span data-stu-id="25394-111">DESCRIPTION</span></span>
<span data-ttu-id="25394-112">**Set-AzStorageAccountManagementPolicy** Cmdlet은 Azure 저장소 계정의 관리 정책을 만들거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="25394-113">예제의</span><span class="sxs-lookup"><span data-stu-id="25394-113">EXAMPLES</span></span>

### <span data-ttu-id="25394-114">예제 1: ManagementPolicy 규칙 개체를 사용 하 여 저장소 계정의 관리 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
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

<span data-ttu-id="25394-115">이 명령은 먼저 관리 정책 규칙 개체를 두 개 만든 다음 2 ManagementPolicy rule 개체를 사용 하 여 저장소 계정의 관리 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="25394-116">예제 2: Json 형식 정책을 사용 하 여 저장소 계정의 관리 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled="true";
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=30;
                    TierToArchive=50;
                    Delete=100;
                });
                Snapshot=(@{
                    Delete=100
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled="false";
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=80;
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
                             "Enabled":  true,
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

<span data-ttu-id="25394-117">이 명령은 json 형식 정책을 사용 하 여 저장소 계정의 관리 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="25394-118">예제 3: 저장소 계정에서 관리 정책을 가져온 다음이를 다른 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="25394-119">이 명령은 먼저 저장소 계정에서 관리 정책을 가져온 다음이를 다른 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="25394-120">변수</span><span class="sxs-lookup"><span data-stu-id="25394-120">PARAMETERS</span></span>

### <span data-ttu-id="25394-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25394-121">-DefaultProfile</span></span>
<span data-ttu-id="25394-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25394-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25394-123">-정책</span><span class="sxs-lookup"><span data-stu-id="25394-123">-Policy</span></span>
<span data-ttu-id="25394-124">설정할 관리 정책 개체</span><span class="sxs-lookup"><span data-stu-id="25394-124">Management Policy Object to Set</span></span>

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

### <span data-ttu-id="25394-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25394-125">-ResourceGroupName</span></span>
<span data-ttu-id="25394-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25394-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="25394-127">-규칙</span><span class="sxs-lookup"><span data-stu-id="25394-127">-Rule</span></span>
<span data-ttu-id="25394-128">관리 정책 규칙</span><span class="sxs-lookup"><span data-stu-id="25394-128">The Management Policy rules.</span></span> <span data-ttu-id="25394-129">New-AzStorageAccountManagementPolicyRule cmdlet을 사용 하 여 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25394-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

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

### <span data-ttu-id="25394-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="25394-130">-StorageAccount</span></span>
<span data-ttu-id="25394-131">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="25394-131">Storage account object</span></span>

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

### <span data-ttu-id="25394-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25394-132">-StorageAccountName</span></span>
<span data-ttu-id="25394-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25394-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="25394-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="25394-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="25394-135">저장소 계정 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="25394-135">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="25394-136">-확인</span><span class="sxs-lookup"><span data-stu-id="25394-136">-Confirm</span></span>
<span data-ttu-id="25394-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25394-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25394-138">-WhatIf</span></span>
<span data-ttu-id="25394-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="25394-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25394-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25394-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25394-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25394-141">CommonParameters</span></span>
<span data-ttu-id="25394-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25394-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25394-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25394-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25394-144">입력</span><span class="sxs-lookup"><span data-stu-id="25394-144">INPUTS</span></span>

### <span data-ttu-id="25394-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="25394-145">System.String</span></span>

## <span data-ttu-id="25394-146">출력</span><span class="sxs-lookup"><span data-stu-id="25394-146">OUTPUTS</span></span>

### <span data-ttu-id="25394-147">Microsoft. PSManagementPolicy./. m a i 관리 정책</span><span class="sxs-lookup"><span data-stu-id="25394-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="25394-148">상속자</span><span class="sxs-lookup"><span data-stu-id="25394-148">NOTES</span></span>

## <span data-ttu-id="25394-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25394-149">RELATED LINKS</span></span>
